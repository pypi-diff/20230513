# Comparing `tmp/generation_models-0.1.0.tar.gz` & `tmp/generation_models-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "generation_models-0.1.0.tar", max compression
+gzip compressed data, was "generation_models-0.2.0.tar", max compression
```

## Comparing `generation_models-0.1.0.tar` & `generation_models-0.2.0.tar`

### file list

```diff
@@ -1,4 +1,4 @@
--rw-r--r--   0        0        0    31749 2023-04-06 18:21:18.071286 generation_models-0.1.0/generation_models.py
--rw-r--r--   0        0        0      352 2023-04-06 19:59:24.208609 generation_models-0.1.0/pyproject.toml
--rw-r--r--   0        0        0      577 1970-01-01 00:00:00.000000 generation_models-0.1.0/setup.py
--rw-r--r--   0        0        0      474 1970-01-01 00:00:00.000000 generation_models-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0    33527 2023-05-12 21:53:55.261646 generation_models-0.2.0/generation_models.py
+-rw-r--r--   0        0        0      600 2023-05-12 22:00:03.663359 generation_models-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0      577 1970-01-01 00:00:00.000000 generation_models-0.2.0/setup.py
+-rw-r--r--   0        0        0      474 1970-01-01 00:00:00.000000 generation_models-0.2.0/PKG-INFO
```

### Comparing `generation_models-0.1.0/generation_models.py` & `generation_models-0.2.0/generation_models.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 from __future__ import annotations
 from enum import Enum
 
 from pydantic import BaseModel, ValidationError, Field, validator, root_validator, parse_obj_as
 from pydantic.fields import Validator
 import typing as t
 from typing_extensions import Annotated
+from numpy import mod
 
 
 def optional_discriminators(unions: t.List[str]):
     def dec(model: t.Type[BaseModel]):
         for k in unions:
             field = model.__fields__[k]
             discriminator_lookup = {v.type_: k for k, v in field.sub_fields_mapping.items()}
@@ -142,52 +143,90 @@
         return values
 
     def __len__(self) -> int:
         for v in (self.up or dict()).values():
             return len(v)
 
 
-class BaseSingleMarket(BaseModel):
-    market_type: t.Optional[t.Literal["single"]] = "single"
-    energy_prices: t.List[float]
-    time_interval_mins: t.Optional[int] = 60
-
-
 class DARTPrices(BaseModel):
     """Mirrors Pandera schema used by the library, but allows for columns of different length, so that users can
     pass, e.g., 5M RTM prices and 1H DAM prices"""
 
     rtm: t.List[float]
     dam: t.List[float]
+    rtorpa: t.Optional[t.List[float]]
+
+    @root_validator(skip_on_failure=True)
+    def check_rtorpa_len(cls, values):
+        if values["rtorpa"]:
+            assert len(values["rtorpa"]) == len(values["rtm"]), "RTORPA must have same lenght as RTM"
+        return values
 
 
 def _check_time_interval(sub_hourly, hourly, time_interval_mins, subhourly_str, hourly_str):
     rt_intervals_per_hour, err = divmod(len(sub_hourly), len(hourly))
     assert err == 0, f"length of {hourly_str} must divide length of {subhourly_str}"
     assert (
         60 / rt_intervals_per_hour == time_interval_mins
     ), f"lengths of {subhourly_str} and {hourly_str} must reflect time_interval_mins"
 
 
-class BaseMultiMarket(BaseModel):
-    market_type: t.Optional[t.Literal["multi"]] = "multi"
-    energy_prices: DARTPrices
+class PriceScenarios(BaseModel):
+    prices: t.List[t.List[float]]
+    weights: t.List[float]
+
+    @root_validator(skip_on_failure=True)
+    def check_weight_length(cls, values):
+        assert len(values["weights"]) == len(values["prices"]), "length of weights must equal length of prices"
+        return values
+
+    @validator("prices")
+    def check_price_lengths(cls, v):
+        # assert all prices have the same lengths
+        l0 = len(v[0])
+        assert all(len(v1) == l0 for v1 in v), "all prices must have the same length"
+        return v
+
+    def __len__(self):
+        return len(self.prices[0])
+
+    @property
+    def shape(self):
+        return len(self.prices), len(self.prices[0])
+
+
+class DARTPriceScenarios(BaseModel):
+    dam: PriceScenarios
+    rtm: PriceScenarios
+
+    @root_validator(skip_on_failure=True)
+    def check_equal_lengths(cls, values):
+        assert values["dam"].shape[1] == values["rtm"].shape[1]
+        return values
+
+    def __len__(self):
+        return self.dam.shape[1]
+
+
+class MarketBase(BaseModel):
+    energy_prices: t.Union[DARTPrices, t.List[float], DARTPriceScenarios]
     reserve_markets: t.Optional[ReserveMarkets]
     time_interval_mins: t.Optional[int] = 60
     load_peak_reduction: t.Optional[LoadPeakReduction]
 
     @root_validator(skip_on_failure=True)
     def check_time_interval(cls, values):
-        _check_time_interval(
-            values["energy_prices"].rtm,
-            values["energy_prices"].dam,
-            values["time_interval_mins"],
-            "rtm prices",
-            "dam prices",
-        )
+        if isinstance(values["energy_prices"], DARTPrices):
+            _check_time_interval(
+                values["energy_prices"].rtm,
+                values["energy_prices"].dam,
+                values["time_interval_mins"],
+                "rtm prices",
+                "dam prices",
+            )
         return values
 
     @root_validator(skip_on_failure=True)
     def check_length(cls, values):
         if values["reserve_markets"]:
             _check_lengths(
                 {"dam prices": values["energy_prices"].dam, "reserve market data": values["reserve_markets"]}
@@ -215,15 +254,15 @@
     wdir: t.List[float]
     wspd: t.List[float]
     alb: t.Optional[t.List[float]]
     snow: t.Optional[t.List[float]]
 
     @root_validator(skip_on_failure=True)
     def check_lengths(cls, values):
-        assert len(next(iter(values.values()))) == 8760, "solar resource time series data must have length of 8760"
+        assert mod(len(next(iter(values.values()))), 8760) == 0, "solar resource time series data must represent 1 year"
         try:
             _check_lengths({k: v for k, v in values.items() if v is not None})
         except AssertionError:
             raise AssertionError("solar resource time series data must have consistent lengths")
         return values
 
     def __len__(self) -> int:
@@ -238,14 +277,28 @@
     data: SolarResourceTimeSeries
     monthly_albedo: t.Optional[t.List[float]]
 
     def __len__(self) -> int:
         return len(self.data)
 
 
+class PSMRegion(str, Enum):
+    NorthAmerica = "North America"
+    AsiaPacific = "Asia/Pacific"
+
+
+class SolarResourceLocation(BaseModel):
+    latitude: float
+    longitude: float
+    region: PSMRegion = PSMRegion.NorthAmerica
+
+    class Config:
+        extra = "forbid"
+
+
 class FileComponent(BaseModel):
     path: str
 
 
 class PVModuleCEC(BaseModel):
     bifacial: bool
     a_c: float
@@ -505,37 +558,37 @@
     elif project_term_units == "days":
         return 24 * project_term
     else:  # years
         return 8760 * project_term
 
 
 def _check_time_interval_project_term(
-    signal, signal_str, project_term, time_interval_mins, project_term_units: TermUnits
+    signal_len, signal_str, project_term, time_interval_mins, project_term_units: TermUnits
 ):
     """
     For more on why we treat project_term as an int and validate like we do check out this PR comment:
     https://github.com/Tyba-Energy/generation/pull/186#discussion_r1054578658. The broader PR has even more context
     should it be needed
     """
-    signal_hours = int(len(signal) * (time_interval_mins / 60))
+    signal_hours = int(signal_len * (time_interval_mins / 60))
     project_term_hours = scale_project_term_to_hours(project_term, project_term_units)
     assert (
         project_term_hours == signal_hours
     ), f"project_term, project_term_units, time_interval_mins, and length of {signal_str} must be consistent"
 
 
 class ExternalGenerationModel(BaseGenerationModel):
     losses: t.Union[ACLosses, Losses]
     production_override: ProductionProfile
     system_design: BaseSystemDesign
 
     @root_validator(skip_on_failure=True)
     def check_time_interval_project_term(cls, values):
         _check_time_interval_project_term(
-            values["production_override"],
+            len(values["production_override"]),
             "production_override",
             values["project_term"],
             values["time_interval_mins"],
             values["project_term_units"],
         )
         return values
 
@@ -557,35 +610,45 @@
 
 
 class ArrayDegradationMode(str, Enum):
     linear = "linear"
     compounding = "compounding"
 
 
+def _pv_gen_len(sol_res, pt):
+    if isinstance(sol_res, SolarResource):
+        return len(sol_res) * pt
+    else:
+        return 8760 * pt
+
+
 class PVGenerationModel(BaseGenerationModel):
     generation_type: t.Optional[t.Literal["PV"]] = "PV"
-    solar_resource: t.Union[SolarResource, t.Tuple[float, float]]
+    solar_resource: t.Union[SolarResource, t.Tuple[float, float], SolarResourceLocation]
     inverter: InverterTypes
     pv_module: PVModuleTypes
     layout: Layout = Layout()
     losses: Losses = Losses()
     system_design: PVSystemDesign
     array_degradation_rate: float = 0.005
     array_degradation_mode: ArrayDegradationMode = ArrayDegradationMode.linear
 
     def __len__(self) -> int:
-        if isinstance(self.solar_resource, SolarResource):
-            return len(self.solar_resource) * self.project_term
-        else:
-            return 8760 * self.project_term
-
-    @validator("time_interval_mins")
-    def check_time_interval_mins(cls, v):
-        assert v == 60, "Currently only time_interval_mins of 60 is supported for PVGenerationModel objects"
-        return v
+        return _pv_gen_len(self.solar_resource, self.project_term)
+
+    @root_validator(skip_on_failure=True)
+    def check_time_interval_project_term(cls, values):
+        _check_time_interval_project_term(
+            _pv_gen_len(values["solar_resource"], values["project_term"]),
+            "solar_resource",
+            values["project_term"],
+            values["time_interval_mins"],
+            values["project_term_units"],
+        )
+        return values
 
     @validator("project_term_units")
     def check_project_term_units(cls, v):
         assert v == "years", "Currently only project_term_units of 'years' is supported for PVGenerationModel objects"
         return v
 
 
@@ -643,34 +706,41 @@
             if values[f"{dm}_degradation_model"]:
                 assert (
                     len(getattr(values[f"{dm}_degradation_model"], f"annual_{dm}_derates")) - 1 >= term
                 ), f"annual_{dm}_derates must be long enough to cover battery term"
         return values
 
 
+class EnergyStrategy(str, Enum):
+    da = "DA"
+    rt = "RT"
+    dart = "DART"
+
+
 class StorageSolverOptions(BaseModel):
     cycling_cost_adder: float = 0.0
     annual_cycle_limit: float = None
     disable_intra_interval_variation: bool = False
     window: int = None
     step: int = None
     flexible_solar: bool = False
     symmetric_reg: bool = False
-    dart: bool = False
+    energy_strategy: t.Optional[EnergyStrategy]
+    dart: t.Optional[bool]
     uncertain_soe: bool = True
     dam_annual_cycle_limit: float = None
     no_virtual_trades: bool = False
     initial_soe: float = 0.0
     duration_requirement_on_discharge: bool = True  # True for ERCOT
     solver: t.Optional[str] = None
     solver_config: SolverConfig = SolverConfig()
 
     @root_validator(skip_on_failure=True)
     def check_dam_annual_cycle_limit(cls, values):
-        if values["dam_annual_cycle_limit"] is not None and not values["dart"]:
+        if values["dam_annual_cycle_limit"] is not None and not (values["dart"] or values["energy_strategy"] == "DART"):
             raise AssertionError("dart must be `true` if dam_annual_cycle_limit is set")
         return values
 
     @validator("solver")
     def check_solver_name(cls, v):
         valid_solvers = ["HiGHS", "GLPK", "HiGHS-GLPK", None]
         assert v in valid_solvers, f"solver must be one of {valid_solvers}"
@@ -678,14 +748,25 @@
 
     @root_validator(skip_on_failure=True)
     def check_solver_config(cls, values):
         if values["solver_config"].solver_specific and (values["solver"] not in {"HiGHS", "GLPK"}):
             raise ValueError("solver_specific options may only be passed when using HiGHS or GLPK solver")
         return values
 
+    @root_validator(skip_on_failure=True)
+    def support_deprecated_dart(cls, values):
+        assert not (values["dart"] is not None and values["energy_strategy"] is not None), (
+            "Only one of `dart` or `energy_strategy` may be provided. `dart` is deprecated; use `energy_strategy`"
+            " instead."
+        )
+        if values["energy_strategy"] is None:
+            values["energy_strategy"] = EnergyStrategy.dart if values["dart"] else EnergyStrategy.da
+            values["dart"] = None
+        return values
+
 
 class MultiStorageInputs(StorageSolverOptions):
     batteries: t.List[BatteryParams]
 
     @validator("batteries")
     def check_battery_terms(cls, v):
         if len(v) > 1:  # don't worry about terms if there's only one battery
@@ -697,15 +778,15 @@
 class StorageCoupling(str, Enum):
     ac = "ac"
     dc = "dc"
     hv_ac = "hv_ac"
 
 
 def _get_price_str_and_price(values):
-    if isinstance(values["energy_prices"], DARTPrices):
+    if isinstance(values["energy_prices"], (DARTPrices, DARTPriceScenarios)):
         return "rtm prices", values["energy_prices"].rtm
     return "energy_prices", values["energy_prices"]
 
 
 class PeakWindow(BaseModel):
     mask: t.List[bool]
     price: float
@@ -753,15 +834,21 @@
                 _check_lengths({limit: values[limit], price_str: price})
         return values
 
 
 def _check_degrad_table_length(values: dict):
     if len(values["storage_inputs"].batteries) == 1:
         battery = values["storage_inputs"].batteries[0]
-        pt = values.get("project_term") or values["pv_inputs"].project_term
+        pt = (
+            scale_project_term_to_hours(
+                values.get("project_term") or values["pv_inputs"].project_term,
+                values.get("project_term_units") or values["pv_inputs"].project_term_units,
+            )
+            / 8760
+        )
         for dm in "capacity", "efficiency":
             if dm_ob := getattr(battery, f"{dm}_degradation_model"):
                 tbl_yrs = len(getattr(dm_ob, f"annual_{dm}_derates")) - 1
                 assert tbl_yrs >= pt, f"annual_{dm}_derates must be long enough to cover project/battery term"
     return values
 
 
@@ -774,15 +861,15 @@
             "reg_down" in (values["reserve_markets"].down or dict())
         ), "when storage_inputs.symmetric_reg is True, both reg_up and reg_down reg markets must be provided"
 
     return values
 
 
 @optional_discriminators(["pv_inputs"])
-class PVStorageModelMixin(ImportExportLimitMixin):
+class PVStorageModel(ImportExportLimitMixin, MarketBase):
     project_type: t.Optional[t.Literal["hybrid"]] = "hybrid"
     storage_inputs: MultiStorageInputs
     storage_coupling: StorageCoupling
     pv_inputs: GenerationModel
     enable_grid_charge_year: t.Optional[float]
 
     @property
@@ -817,16 +904,20 @@
             ), "project_term must be greater than or equal to the total battery terms"
         return values
 
     @root_validator(skip_on_failure=True)
     def check_degrad_table_length(cls, values):
         return _check_degrad_table_length(values)
 
+    @root_validator(skip_on_failure=True)
+    def check_sym_reg_inputs(cls, values):
+        return _check_symmetric_reg_inputs(values)
+
 
-class StandaloneStorageModelMixin(ProjectTermMixin, ImportExportLimitMixin):
+class StandaloneStorageModel(ProjectTermMixin, ImportExportLimitMixin, MarketBase):
     project_type: t.Optional[t.Literal["storage"]] = "storage"
     storage_inputs: MultiStorageInputs
     ambient_temp: t.Optional[t.List[float]]
 
     @root_validator(skip_on_failure=True)
     def check_ambient_temp_length(cls, values):
         if values["ambient_temp"]:
@@ -834,15 +925,15 @@
             _check_lengths({price_str: price, "ambient_temp": values["ambient_temp"]})
         return values
 
     @root_validator(skip_on_failure=True)
     def check_time_interval_project_term(cls, values):
         price_str, price = _get_price_str_and_price(values)
         _check_time_interval_project_term(
-            price, price_str, values["project_term"], values["time_interval_mins"], values["project_term_units"]
+            len(price), price_str, values["project_term"], values["time_interval_mins"], values["project_term_units"]
         )
         return values
 
     @root_validator(skip_on_failure=True)
     def check_battery_and_project_terms(cls, values):
         # only validate battery terms if a battery term is passed or multiple batteries are passed
         if len(values["storage_inputs"].batteries) > 1 or values["storage_inputs"].batteries[0].term is not None:
@@ -859,92 +950,57 @@
             ), f"length of {price_str} must be greater than total battery terms"
         return values
 
     @root_validator(skip_on_failure=True)
     def check_degrad_table_length(cls, values):
         return _check_degrad_table_length(values)
 
+    @root_validator(skip_on_failure=True)
+    def check_sym_reg_inputs(cls, values):
+        return _check_symmetric_reg_inputs(values)
+
 
 def get_pv_model(**data: t.Any) -> GenerationModel:
     try:
         m = PVGenerationModel(**data)
     except ValidationError:
         try:
             m = DCExternalGenerationModel(**data)
         except ValidationError:
             m = ACExternalGenerationModel(**data)
     return m
 
 
-class PVStorageSingleMarketModel(PVStorageModelMixin, BaseSingleMarket):
-    pass
-
-
-class PVStorageMultiMarketModel(PVStorageModelMixin, BaseMultiMarket):
-    @root_validator(skip_on_failure=True)
-    def check_sym_reg_inputs(cls, values):
-        return _check_symmetric_reg_inputs(values)
-
-
-PVStorageModel = Annotated[
-    t.Union[PVStorageSingleMarketModel, PVStorageMultiMarketModel], Field(discriminator="market_type")
-]
-
-
 def get_pv_storage_model(**data: t.Any) -> PVStorageModel:
-    try:
-        m = PVStorageMultiMarketModel(**data)
-    except ValidationError:
-        m = PVStorageSingleMarketModel(**data)
-    return m
-
-
-class StandaloneStorageModelSingleMarket(StandaloneStorageModelMixin, BaseSingleMarket):
-    pass
-
-
-class StandaloneStorageModelMultiMarket(StandaloneStorageModelMixin, BaseMultiMarket):
-    @root_validator(skip_on_failure=True)
-    def check_sym_reg_inputs(cls, values):
-        return _check_symmetric_reg_inputs(values)
+    return PVStorageModel(**data)
 
 
-StandaloneStorageModel = Annotated[
-    t.Union[StandaloneStorageModelSingleMarket, StandaloneStorageModelMultiMarket], Field(discriminator="market_type")
-]
-
-
-def get_standalone_storage_model(**data: t.Any) -> StandaloneStorageModel:
-    try:
-        m = StandaloneStorageModelMultiMarket(**data)
-    except ValidationError:
-        m = StandaloneStorageModelSingleMarket(**data)
-    return m
+def get_standalone_storage_model(model: dict) -> StandaloneStorageModel:
+    return StandaloneStorageModel(**model)
 
 
 JobModel = Annotated[
     t.Union[StandaloneStorageModel, PVStorageModel, GenerationModel], Field(discriminator="project_type")
 ]
 
 
+@optional_discriminators(["model"])
 class AsyncModelBase(BaseModel):
     id: str
     model: JobModel
     results_path: t.Optional[str]
 
 
 @optional_discriminators(["model"])
 class AsyncPVModel(AsyncModelBase):
     id: str
     model: GenerationModel
 
 
-@optional_discriminators(["model"])
 class AsyncPVStorageModel(AsyncModelBase):
     id: str
     model: PVStorageModel
 
 
-@optional_discriminators(["model"])
 class AsyncStandaloneStorageModel(AsyncModelBase):
     id: str
     model: StandaloneStorageModel
```

### Comparing `generation_models-0.1.0/setup.py` & `generation_models-0.2.0/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 modules = \
 ['generation_models']
 install_requires = \
 ['pydantic>=1.5.1,<2.0.0']
 
 setup_kwargs = {
     'name': 'generation-models',
-    'version': '0.1.0',
+    'version': '0.2.0',
     'description': 'generation API data model',
     'long_description': 'None',
     'author': 'battery_al',
     'author_email': 'allenlawrence94@gmail.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'None',
```

