# Comparing `tmp/cdx_tf-0.1.1.tar.gz` & `tmp/cdx_tf-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\cdx_tf-0.1.1.tar", last modified: Thu Mar  9 02:22:04 2023, max compression
+gzip compressed data, was "cdx_tf-0.1.2.tar", last modified: Sat May 13 09:50:10 2023, max compression
```

## Comparing `cdx_tf-0.1.1.tar` & `cdx_tf-0.1.2.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxrwxrwx   0        0        0        0 2023-03-09 02:22:04.000000 cdx_tf-0.1.1/
--rw-rw-rw-   0        0        0     1090 2023-03-09 01:49:43.000000 cdx_tf-0.1.1/LICENSE
--rw-rw-rw-   0        0        0      525 2023-03-09 02:22:04.000000 cdx_tf-0.1.1/PKG-INFO
--rw-rw-rw-   0        0        0       84 2023-03-09 01:49:43.000000 cdx_tf-0.1.1/README.md
-drwxrwxrwx   0        0        0        0 2023-03-09 02:22:04.000000 cdx_tf-0.1.1/cdx_tf/
--rw-rw-rw-   0        0        0      126 2023-03-09 02:22:02.000000 cdx_tf-0.1.1/cdx_tf/__init__.py
--rw-rw-rw-   0        0        0     5299 2023-03-09 02:02:59.000000 cdx_tf-0.1.1/cdx_tf/clip.py
--rw-rw-rw-   0        0        0    38664 2023-03-09 02:13:44.000000 cdx_tf-0.1.1/cdx_tf/gym.py
--rw-rw-rw-   0        0        0     3863 2023-03-09 02:12:12.000000 cdx_tf-0.1.1/cdx_tf/layers.py
--rw-rw-rw-   0        0        0     5651 2023-03-09 01:59:12.000000 cdx_tf-0.1.1/cdx_tf/monetary_utility.py
--rw-rw-rw-   0        0        0     2345 2023-03-09 01:59:20.000000 cdx_tf-0.1.1/cdx_tf/optimizer.py
--rw-rw-rw-   0        0        0     9622 2023-03-09 01:57:14.000000 cdx_tf-0.1.1/cdx_tf/util.py
-drwxrwxrwx   0        0        0        0 2023-03-09 02:22:04.000000 cdx_tf-0.1.1/cdx_tf.egg-info/
--rw-rw-rw-   0        0        0      525 2023-03-09 02:22:03.000000 cdx_tf-0.1.1/cdx_tf.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      302 2023-03-09 02:22:03.000000 cdx_tf-0.1.1/cdx_tf.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-03-09 02:22:03.000000 cdx_tf-0.1.1/cdx_tf.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       60 2023-03-09 02:22:03.000000 cdx_tf-0.1.1/cdx_tf.egg-info/requires.txt
--rw-rw-rw-   0        0        0        7 2023-03-09 02:22:03.000000 cdx_tf-0.1.1/cdx_tf.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-03-09 02:22:04.000000 cdx_tf-0.1.1/setup.cfg
--rw-rw-rw-   0        0        0     1816 2023-03-09 01:51:34.000000 cdx_tf-0.1.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 09:50:10.063374 cdx_tf-0.1.2/
+-rw-rw-rw-   0        0        0     1090 2023-03-09 01:49:43.000000 cdx_tf-0.1.2/LICENSE
+-rw-rw-rw-   0        0        0     2716 2023-05-13 09:50:10.061373 cdx_tf-0.1.2/PKG-INFO
+-rw-rw-rw-   0        0        0     2286 2023-03-20 22:12:29.000000 cdx_tf-0.1.2/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 09:50:10.026377 cdx_tf-0.1.2/cdx_tf/
+-rw-rw-rw-   0        0        0      126 2023-05-13 09:50:07.000000 cdx_tf-0.1.2/cdx_tf/__init__.py
+-rw-rw-rw-   0        0        0     5461 2023-05-13 09:28:16.000000 cdx_tf-0.1.2/cdx_tf/clip.py
+-rw-rw-rw-   0        0        0    72406 2023-05-13 09:31:45.000000 cdx_tf-0.1.2/cdx_tf/gym.py
+-rw-rw-rw-   0        0        0    42122 2023-05-13 09:31:14.000000 cdx_tf-0.1.2/cdx_tf/models.py
+-rw-rw-rw-   0        0        0    19005 2023-05-13 09:29:54.000000 cdx_tf-0.1.2/cdx_tf/monetary_utility.py
+-rw-rw-rw-   0        0        0     2323 2023-05-13 09:29:54.000000 cdx_tf-0.1.2/cdx_tf/optimizer.py
+-rw-rw-rw-   0        0        0    10962 2023-04-15 17:30:23.000000 cdx_tf-0.1.2/cdx_tf/util.py
+drwxrwxrwx   0        0        0        0 2023-05-13 09:50:10.059372 cdx_tf-0.1.2/cdx_tf.egg-info/
+-rw-rw-rw-   0        0        0     2716 2023-05-13 09:50:09.000000 cdx_tf-0.1.2/cdx_tf.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      302 2023-05-13 09:50:09.000000 cdx_tf-0.1.2/cdx_tf.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 09:50:09.000000 cdx_tf-0.1.2/cdx_tf.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      116 2023-05-13 09:50:09.000000 cdx_tf-0.1.2/cdx_tf.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        7 2023-05-13 09:50:09.000000 cdx_tf-0.1.2/cdx_tf.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 09:50:10.063374 cdx_tf-0.1.2/setup.cfg
+-rw-rw-rw-   0        0        0      908 2023-05-13 09:50:07.000000 cdx_tf-0.1.2/setup.py
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `cdx_tf-0.1.1/LICENSE` & `cdx_tf-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `cdx_tf-0.1.1/cdx_tf/clip.py` & `cdx_tf-0.1.2/cdx_tf/clip.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,89 +1,89 @@
 """
 Various methods for clipping
------------------------------
+----------------------------
+
 March 1st, 2023
 @author: hansbuehler
 """
 
 from cdxbasics.logger import Logger
-from cdxbasics.config import Config
+from cdxbasics.config import Config, Float, Int#NOQA
 from .util import tf, def_dtype
 _log = Logger(__file__)
 
-@tf.function
-def hard_clip( x : tf.Tensor, x_min : tf.Tensor, x_max : tf.Tensor, validate_bounds : bool = False ) -> tf.Tensor:
+@tf.function(reduce_retracing=True)
+def tf_hard_clip( x : tf.Tensor, x_min : tf.Tensor, x_max : tf.Tensor, validate_bounds : bool = False ) -> tuple:
     """
-    Hard clips x between 'x_max' and 'x_min' with quadratic penalty on exceeding the bounds.
+    Hard clips x between 'x_max' and 'x_min', and returns both the new value and a quadratic penalty on exceeding the bounds.
     The functiuon will compute y min( max_x, max( min_x )) and return (y, abs(x-y)**2 )
-    
+
     Parameters
     ----------
         x : tf.Tensor
         x_max, x_min: tf.Tensor
             Bounds
-        validate_bounds : if True, check that x_min<x_max
-        
+        validate_bounds :
+            If True, check that x_min<=x_max and throw an exception if that is not True
+            If False, the x will be set to the average of x_min and x_max whenever they are in the wrong order.
+
     Returns
     -------
         Returns a tuple x, and p:
             x : truncated value for x
             p : penalty of the form (x-x_new)**2 which should be added to the overall training objective
                 to ensure there is a gradient towards the interior of the clip
-    
+
     """
     if not validate_bounds:
-        x_ = tf.where( maxx > minx, tf.clip_by_value( x, minx, maxx ), 0.5*(maxx+minx) )
+        x_ = tf.where( x_max > x_min, tf.clip_by_value( x, x_min, x_max ), 0.5*(x_max+x_min) )
         p  = tf.math.abs( x - x_ ) ** 2
         return x_, p
-    with tf.control_dependencies( [ tf.debugging.assert_greate( maxx, minx, message="Upper bound for trades must be bigger than lower bound" ) ] ):
-        return hard_clip( x, x_min, x_max, validate_bounds = False )
-    
+    with tf.control_dependencies( [ tf.debugging.assert_greater( x_max, x_min, message="Upper bound for trades must be bigger than lower bound" ) ] ):
+        return tf_hard_clip( x, x_min, x_max, validate_bounds = False )
+
 try:
     import tensorflow_probability as tfp
 except:
-    tfp = None 
-   
+    tfp = None
+
 class SoftClip(tf.keras.layers.Layer):
     """
     Simple wrapper around tensorflow_probability.bijectors.SoftClip with a number of features
     Additional config variables are
         hard_clip: hard clip, no soft clipping (this is intended for debugging)
         outer_clip: appy outer clip, e.g. hard clip beyond an excessive rannge
         outer_clip_cut_off: bounds for the outer clip
     """
 
     def __init__(self, config, name : str = None, dtype : tf.DType = def_dtype ):
-        """
-        Initialize softclip from tensorflow_probability
-        """
-        tf.keras.layers.Layer.__init__(self, name=name, dtype=dtype )   
-        _log.verify( not tfp is None, "tensorflow_probability package not found")      
-        
+        """ Initialize softclip from tensorflow_probability """
+        tf.keras.layers.Layer.__init__(self, name=name, dtype=dtype )
+        _log.verify( not tfp is None, "tensorflow_probability package not found")
+
         self.hard_clip             = config('hard_clip', False, bool, "Use min/max instread of soft clip for limiting actions by their bounds")
         self.outer_clip            = config('outer_clip', True, bool, "Apply a hard clip 'outer_clip_cut_off' times the boundaries")
         self.outer_clip_cut_off    = config('outer_clip_cut_off', 10., Float>=1., "Multiplier on bounds for outer_clip")
         hinge_softness             = config('softclip_hinge_softness', 1., Float>0., "Specifies softness of bounding actions between lbnd_a and ubnd_a")
         self.softclip              = tfp.bijectors.SoftClip( low=0., high=1., hinge_softness=hinge_softness, name='soft_clip' if name is None else name )
         config.done()
-    
+
     def __call__( self, actions, lbnd_a, ubnd_a ):
         """ Clip the action within lbnd_a, ubnd_a """
-        
         with tf.control_dependencies( [ tf.debugging.assert_greater_equal( ubnd_a, lbnd_a, message="Upper bound for actions must be bigger than lower bound" ),
                                         tf.debugging.assert_greater_equal( ubnd_a, 0., message="Upper bound for actions must not be negative" ),
                                         tf.debugging.assert_less_equal( lbnd_a, 0., message="Lower bound for actions must not be positive" ) ] ):
-        
+
             if self.hard_clip:
                 # hard clip
                 # this is recommended for debugging only.
                 # soft clipping should lead to smoother gradients
                 actions = tf.minimum( actions, ubnd_a, name="hard_clip_min" )
                 actions = tf.maximum( actions, lbnd_a, name="hard_clip_max" )
-                return actions            
+                return actions
 
             if self.outer_clip:
                 # to avoid very numerical errors due to very
                 # large pre-clip actions, we cap pre-clip values
                 # hard at 10 times the bounds.
                 # This can happen if an action has no effect
                 # on the gains process (e.g. hedge == 0)
```

### Comparing `cdx_tf-0.1.1/cdx_tf/gym.py` & `cdx_tf-0.1.2/cdx_tf/models.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,778 +1,842 @@
 """
-Keras Model base class for Gym models
--------------------------------------
-* Cachable
-* Keeps best state
-* Optimized for async training
+Utilities to build keras models
+-------------------------------
 
-Feb 25, 2023
+Below defines a number of utility functions to generate keras models.
+
+The most atomic models are
+    * VariableModel which represents a variable.
+      The added functionality is that its __call__() function will scale the variable to the sample size
+      correctly, e.g. if the variable if of size (2,3) then __call__() will return (batch_size, 2, 3).
+    * DenseModel which represents a fully conencted neural network
+      It also has a zero_mode which initializes the network such that the initial value is zero,
+      while derivatives are randomized.
+
+The two atomic models are wrapped up into a function call
+    * dense_model()
+      This function creates either a DenseModel or a VariableModel, depending on whether the size of the
+      input features: if it is zero, a VariableModel will be returned.
+      dense_model() implements also defaulting for user variables and configuration handling
+
+The two top level models are
+    * DenseAgent()
+      A keras model representing a fully connected model which is parameterized by the 'features' it extracts
+      from the 'data' feature set.
+    * RecurrentAgent()
+      A recurrent agent with the same functionality as DenseAgent, which also allows for recurrent nodes.
+
+April 1st, 2023
 @author: hansbuehler
 """
-from collections.abc import Mapping
-from cdxbasics.config import Config, Int, Float
-from cdxbasics.verbose import Context
+
 from cdxbasics.logger import Logger
-from cdxbasics.prettydict import PrettyDict as PrettyDict
-from cdxbasics.util import uniqueHash, fmt_now, fmt_seconds
-from cdxbasics.subdir import SubDir, uniqueFileName48, CacheMode
-from cdx_tf.util import npCast, tfCast, def_dtype
-from cdx_tf.optimizer import create_optimizer
-import tensorflow as tf
+from cdxbasics.util import fmt_list
+from cdxbasics.config import Config, Float, Int, to_config # NOQA
+from collections.abc import Mapping
 import numpy as np
-import time as time
-
+from .util import tf, def_dtype, tf_make_dim
 _log = Logger(__file__)
 
-dtype = def_dtype
+def name(self):
+    return self.name if not self.name is None else type(self).__name__
 
-MODEL_FILE = "gym.h5"
-PROGRESS_FILE = "progress"
+# =====================================================================================
+# Raw building blocks
+# These models will expect tensors of a specified input dimension in __call__()
+# =====================================================================================
 
-# ==========================================================================
-# Model
-# Cachable gym
-# ==========================================================================
-
-class Gym(tf.keras.Model):
-    """ 
-    Base class for a keras gym model with
-    * Automatic caching
-    * Default tracking of progress, with support for asynchronous training
-
-    This gym assumes that the loss of the gym is "linear", e.g. an expectation of a returned variable (usually 'loss')
-    
-    Implementation comments
-    -----------------------
-    In order to implement your own gym,
-        1) derive from gym
-        2) implement build/call.
-           The data passed to each will be of the form of the dictionaries in environment.trn.tf_data.
-        3) Set the class variable CACHE_VERSION to a string version
-        4) Implement from_config / get_config. Without doing this, the system cannot create/restore the gym from a cache
+class VariableModel( tf.keras.Model ):
     """
-    
-    CACHE_VERSION = "0.0.1"
-    
-    def __init__(self, config          : Config,
-                       name            : str = None,
-                       dtype           : tf.DType = None,
-                       trainable       : bool = True,
-                       cache_uid       : str = None ):
-        """
-        Initializes the cachable gym
-        ------------------------------
-            cache_uid : Config or str
-                Unique ID for this gym for caching.
-                You can pass a 'Config' object in which case it will call config_ID.cache_unique_id.
-            name : str
-                Name of the object
-            dtype : tf.DType
-                Type of the gym
-            trainable : bool
-                Whether the gym is trainable.
-            cache_version : int
-                Additional version for the cache. This allows updating caches even if no config changes (e.g when a bug in the code was found)
+    Keras Model which represents a variable.
+
+    The complication here is that such a model does not naturally get informed about the batch dimension of the
+    data is it supposed to return. The example code hacks this by looking up *any* member of the 'data' provided
+    to call(), and scale the variable accordingly.
+    """
+
+    def __init__(self,
+                 init,
+                 dtype     : tf.DType = def_dtype,
+                 name      : str = None,
+                 trainable : bool = True):
         """
-        tf.keras.Model.__init__(self, name=name, dtype=dtype, trainable=trainable )
+        Initialie the variable model for a given variable. The model does not take any inputs but returns the
+        value of the variable, scaled up to the batch size.
 
-        _log.verify( isinstance(config, Config), "'config' must be of type '%s' but appears to be of type '%s'", Config.__name__, type(config).__name__ )
-        self._cache_unique_id = config.unique_id() if cache_uid is None else str(cache_uid)
-        self._cache_config    = config.copy() 
-        
-    # -------------------
-    # syntatic sugar
-    # -------------------
+        Parameters
+        ----------
+            init:
+                If an int: initialize with a zero vector of length init
+                If a shape: initialize with a zero vector of shape init
+                If a numpy array: initialize with this array
+            dtype, name, trainable: c.f. tf.keras.Model()
+        """
+        tf.keras.Model.__init__(self, name=name, dtype=dtype, trainable=trainable )
+        if isinstance(init, int):
+            init = np.zeros(shape=(init,))
+        elif isinstance(init, (tuple,list)):
+            init = np.zeros(shape=tuple(init))
+        else:
+            init = np.asarray( init )
+        self._init     = init
+        self._variable = tf.Variable( init, trainable=trainable, name="var_" + self.name, dtype=self.dtype )
+
+    def call(self, data, training=False):
+        """ Returns the variable, scaled to the current batch size. For this to work, 'data' must contain at least one correct data element """
+        assert isinstance( data, (Mapping, tf.Tensor) ), "'data' must be a tensor or a dict, not %s" % type(data).__name__
+        def zeros_from_data( data ) -> tf.Tensor:
+            """ Returns a zero tensor of dimension one, with the first dimension equal to the batch size """
+            if isinstance(data, tf.Tensor):
+                while len(data.shape) > 1:
+                    data = data[:,0]
+                return data*0.
+            assert isinstance(data, Mapping), "'data' must be a tensor or a dictionary. Found %s" % type(data).__name__
+            for t in data:
+                t = data[t]
+                d = zeros_from_data(t)
+                if not d is None:
+                    return d
+            return None
+
+        zero = zeros_from_data(data)
+        _log.verify( not zero is None, "Cannot determine batch sample size from 'data' of type %s", type(data).__name__ )
+        zero = tf_make_dim( zero, len(self._variable.shape)+1 )
+        return zero + self._variable[None,...]
 
     @property
     def num_trainable_weights(self) -> int:
-        """ Returns the number of weights. The gym must have been call()ed once """
+        """
+        Returns the number of weights. The gym must have been call()ed once
+        Agent needs to have been called at least once
+        """
         weights = self.trainable_weights
         return np.sum( [ np.prod( w.get_shape() ) for w in weights ] ) if not weights is None else 0.
-        
+
     @property
-    def cache_uid( self ):
-        """ Return the unique ID for this gym. """
-        return self._cache_unique_id
-    
-    @property
-    def cache_def_directory_name( self ):
-        """ Returns a descriptive name for this class which can be used as directory for the caches. No trailing '/' """
-        name = str( self.__class__.__name__ )
-        return name if self._cache_version is None else ( name + "/" + self._cache_version )
-
-    # -------------------
-    # Keras serialization    
-    # -------------------
-
-    @staticmethod
-    def from_config( tf_config : dict ):
-        """
-        You will have to implement this for all derived classes.
-        Default pattern is written below        
-        """
-        raise NotImplementedError("Please implement Gym.from_config")
-        
-    @staticmethod
-    def from_config_default( Class : type, tf_config : dict ):
-        """
-        Default 'from_config' code.
-        Meant to be used as
-        
-        class MyGyum(Gym):
-            
-            @staticmethod
-            def from_config( tf_config : dict ):
-                return Gym.from_config_default( MyGym, tf_config )
-        """
-        _log.verify( tf_config['cache_version'] == CACHE_VERSION, "Error reading configuration from cache for '%s'': version mismatch. Found version %s, but current code is version %s", Class.__name__, tf_config['cache_version'], Class.CACHE_VERSION )        
-        return Class( config        = tf_config['config'],
-                      name          = tf_config['name'],
-                      dtype         = tf_config['dtype'],
-                      trainable     = tf_config['trainable']
-                )
-        
-    def get_config( self ):
-        """ You will need to overwrite this if your __init__ signature changes """
-        return dict(
-            config        = self._cache_config,
-            name          = self.name,
-            dtype         = self.type,
-            trainable     = self.trainable,
-            cache_version = self.CACHE_VERSION
-            )
-
-
-# ==========================================================================
-# TrainingInfo
-# Information on the current training run
-# ==========================================================================
+    def variable(self) -> tf.Variable:
+        """ Return underlying TF variable """
+        return self._variable
+
+    def get_config(self) -> dict:#NOQA
+        return dict( init = self._init, dtype=self.dtype, name=self.name, trainable=self.trainable )
 
-class TrainingInfo(object):
+class DenseModel( tf.keras.Model ):
     """
-    Information on the current training run for user updates
+    Standard dense Sequential keras neural network.
+
+    Represents a dense network with a given 'depth', 'width', 'activation' function and a final layer with activation function 'final_act' (typicall linear).
+    The layer maps a tensors of dimension nInput into tensors of dimension nOutput.
+
+    The model can initialize the model with zero initial value, but with non-trivial initial gradients.
+    It does this by returning the difference between two networks, with the same initial weights, but where only
+    the first is trainable.
+
+    If the number of inputs is zero, then this function uses a VariableModel initialized at zero.
     """
-    
-    def __init__(self, *, batch_size, epochs ):#NOQA
-        self.epochs       = epochs       # total epochs requested by the user. Note that the actual epochs will be reduced by the number of epochs already trained in the cached file
-        self.batch_size   = batch_size   # batch size.
-
-# ==========================================================================
-# Environment
-# Contains the top level data available throughout the training process
-# ==========================================================================
-
-class Environment( PrettyDict ):
-    """ 
-    Represents the data available for the overall training loop: the gym model, its data, sample weights.
-    This means this environment can also execute a predict() on the current gym for both its training and validation set.
-    This is implemented in predict().
-    
-    Objects of this class are not serialized directly.
-    
-    The usual step is to create one's own, e.g. to add additional environment data
+
+    def __init__(self,  nInput     : int,
+                        nOutput    : int,
+                        width      : int = 50,
+                        depth      : int = 3,
+                        activation : str = "relu",
+                        final_act  : str = "linear",
+                        zero_model : bool = False,
+                        regression : bool = False,
+                        dtype      : tf.DType = def_dtype,
+                        name       : str = None,
+                        trainable  : bool = True
+                    ):
+        """
+        Represents a dense network with a given 'depth', 'width', 'activation' function and a final layer with activation function 'final_act' (typicall linear).
+        The layer maps a tensors of dimension nInput into tensors of dimension nOutput.
+
+        Parameters
+        ----------
+            nInput :
+                second dimension of the input vector to this model, e.g. it expects tensors of shape [None, nInput]
+                If nInput is zero, then this function returns a VariableModel( nOutput )
+            nOutput:
+                number of output states
+            network construction:
+                width        : width of the network
+                depth        : depth
+                activation   : activation function in core network
+                final_activation : activation function to compress last 'width' to nOutput. Usually linear.
+                zero_model   : whether the model is initialzed to zero initial value (but not zero gradients)
+                               Practically, the model constructs both the original model F and a non-trainable
+                               model F', then sets the weights of F' to the initial weights of F, and defines
+                               the full model as M=F-F'. If 'trainable' is False then this function returnbs a network
+                               with zero initial value.
+                regression   : hard set the network to a pure regression model.
+                               This is equivalent to setting depth = 0, width = nInput, and final_activation = 'linear'.
+            dtype, name, trainable :
+                see tf.keras.Model()
+        """
+        tf.keras.Model.__init__(self, name=name, dtype=dtype, trainable=trainable )
+
+        self._nInput      = int(nInput)
+        self._nOutput     = int(nOutput)
+        assert self._nInput > 0, nInput
+        assert self._nOutput > 0, nOutput
+
+        self._get_config = dict( nInput     = self._nInput,
+                                 nOutput    = self._nOutput,
+                                 width      = width,
+                                 depth      = depth,
+                                 activation = activation,
+                                 final_act  = final_act,
+                                 zero_model = zero_model,
+                                 regression = regression,
+                                 dtype      = dtype,
+                                 name       = name,
+                                 trainable = trainable)
+
+        if regression:
+            depth      = 0
+            width      = nInput
+            final_act  = 'linear'
+
+        def dense(width,activation, x1, x2 ):
+            """ Utility function to construct zero_model layers """
+            d1 = tf.keras.layers.Dense(units=width,
+                                       activation=activation,
+                                       use_bias=True, dtype=dtype,
+                                       trainable=trainable )
+            if x2 is None:
+                return d1(x1), None
+
+            d2 = tf.keras.layers.Dense(units=width,
+                                       activation=activation,
+                                       use_bias=True, dtype=dtype,
+                                       trainable=False )
+            x1 = d1(x1)
+            x2 = d2(x2)
+            return x1, x2
+
+        inp       = tf.keras.layers.Input( shape=(nInput,), dtype=dtype )
+        x1, x2    = ( inp, inp if zero_model else None )
+        for d in range(depth):
+            x1, x2    = dense( width, activation, x1, x2 )
+        x1, x2 = dense( nOutput, final_act, x1, x2 )
+        x  = tf.keras.layers.Subtract()([x1, x2]) if not x2 is None else x1
+        m  = tf.keras.Model( inputs=inp, outputs=x, name=name )
+        if zero_model:
+            for v1, v2 in zip( m.trainable_weights, m.non_trainable_weights ):
+                v2.assign( v1.value() )
+        self._model = m
+
+    def __call__(self, features : tf.Tensor, **kwargs ) -> tf.Tensor:
+        """ Execute model. """
+        assert isinstance( features, tf.Tensor ), "'features' must be a tensor, not %s" % type(features).__name__
+        _log.verify( len(features.shape) == 2 and int(features.shape[1]) == self._nInput, "Model '%s' input error: expected features tensor of shape [None, %ld] but found tensor of shape %s", name(self) , self._nInput, features.shape.as_list() )
+        return self._model(features,**kwargs)
+
+    def get_config(self) -> dict:#NOQA
+        return self._get_config
+
+    @property
+    def num_trainable_weights(self) -> int:
+        """
+        Returns the number of weights. The gym must have been call()ed once
+        Agent needs to have been called at least once
+        """
+        weights = self.trainable_weights
+        return np.sum( [ np.prod( w.get_shape() ) for w in weights ] ) if not weights is None else 0.
+
+
+def dense_model( nInput     : int,
+                 nOutput    : int,
+                 config     : Config = None,
+                 kwargs_cfg : dict = None,
+                 **kwargs
+                 ) -> tf.keras.Model:
+    """
+    Create standard dense Sequential keras neural network.
+
+    The function creates a dense network of 'depth' and 'width' with activation function 'activation'.
+    The final layer then condenses the last 'width' nodes to 'nOutput' nodes, usually with a linear 'final_act'.
+    The model can initialize the model with zero initial value, but with non-trivial initial gradients.
+    It does this by returning the difference between two networks, with the same initial weights, but where only
+    the first is trainable.
+
+    The function takes in a 'config' which lets a user set the geometry of the network, and default values set
+    by the code developer.
+
+    This function expects data to be passed as a tensor of dimension [None, nInput].
+    See Agent() for a model which can extract named elements from a feature dictionary on the fly.
+
+    If the number of inputs is zero, then this function returns a VariableModel initialized at zero.
+
+    Parameters
+    ----------
+        nInput :
+            second dimension of the input vector to this model, e.g. it expects tensors of shape [None, nInput]
+            If nInput is zero, then this function returns a VariableModel( nOutput )
+        nOutput:
+            number of output states
+
+        kwargs_cfg, **kwargs :
+            Only one of the these two can be non-empty.
+            User settings to specify the following:
+                width        : width of the network
+                depth        : depth
+                activation   : activation function in core network
+                final_activation : activation function to compress last 'width' to nOutput. Usually linear.
+                zero_model   : whether the model is initialzed to zero initial value (but not zero gradients)
+                               Practically, the model constructs both the original model F and a non-trainable
+                               model F', then sets the weights of F' to the initial weights of F, and defines
+                               the full model as M=F-F'. If 'trainable' is False then this function returnbs a network
+                               with zero initial value.
+                regression   : hard set the network to a pure regression model.
+                               This is equivalent to setting depth = 0, width = nInput, and final_activation = 'linear'.
+
+                Each of the above can either be specified directly, or they can be read from a Config dictrionary.
+                In that case the function still allows providing default values.
+
+                For example, instead of setting width=50, we may pass a Config object with config=config, and also a default
+                value def_width=50.
+
+            dtype, name, trainable :
+                see tf.keras.Model()
+    Returns
+    -------
+        Keras model.
+    """
+    assert kwargs_cfg is None or len(kwargs) == 0, "Cannot specify 'kwargs_cfg' and **kwargs"
+    kwargs          = to_config(kwargs_cfg if not kwargs_cfg is None else kwargs, config_name="kwargs_dense_model")
+
+    width           = kwargs('width', None, (None, Int>0))
+    depth           = kwargs('depth', None, (None, Int>=0))
+    activation      = kwargs('activation', None, (None, str))
+    final_act       = kwargs('final_act', None, (None,str))
+    zero_model      = kwargs('zero_model', None, (None, bool))
+    regression      = kwargs('regression', None, (None, bool))
+
+    dtype           = kwargs('dtype', def_dtype )
+    name            = kwargs('name', None, (str, None))
+    trainable       = kwargs('trainable', True, bool)
+
+    def_width       = kwargs("def_width", 50, Int>0 )
+    def_depth       = kwargs("def_depth", 3, Int>=0 )
+    def_activation  = kwargs("def_activation", 'relu', str)
+    def_final_act   = kwargs("def_final_act", "linear", str)
+    def_zero_model  = kwargs("def_zero_model", True, bool)
+    def_regression  = kwargs("def_regression", False, bool)
+
+    kwargs.done() # catch developer typos
+
+    config          = config if not config is None else Config()
+    width           = config("width", def_width, Int>0, "Width") if width is None else width
+    depth           = config("depth", def_depth, Int>=0, "Depth") if depth is None else depth
+    activation      = config("activation", def_activation, str, "Activation function") if activation is None else activation
+    final_act       = config("final_activation",def_final_act, str, "Final activation function") if final_act is None else final_act
+    zero_model      = config("zero_model", def_zero_model, bool, "Whether to initialze values (but not derivatives) of the model with zero") if zero_model is None else zero_model
+    regression      = config("simple_regression", def_regression, bool, "Learn simple regression model only") if regression is None else regression
+
+    config.done() # catch user errors
+
+    if nInput == 0:
+        return VariableModel( int(nOutput), name=name, dtype=dtype, trainable=trainable )
+
+    return DenseModel( nInput  = nInput,
+                       nOutput = nOutput,
+                       width   = width,
+                       depth   = depth,
+                       activation = activation,
+                       final_act  = final_act,
+                       zero_model = zero_model,
+                       regression = regression,
+                       dtype = dtype,
+                       name = name,
+                       trainable = trainable)
+
+# =====================================================================================
+# Agents
+# Agents extract named features from the 'data' given to __call__
+# =====================================================================================
+
+class DenseAgent(tf.keras.Model):
     """
-    
-    def __init__(self, *, gym                : Gym,
-                          tf_trn_data        : dict,
-                          tf_val_data        : dict = None,
-                          trn_sample_weights : np.ndarray = None,
-                          val_sample_weights : np.ndarray = None,
-                          key_loss           : str = "loss",
-                          **kwargs ):
-        """
-        Initialize environment.
-        The gym is set as part of training via set_model (e.g. if the gym was restored from a cache)
-        
+    Standardized generic agent which will use named features as inputs, and will extract those from the 'data' dictionary provided.
+    All features are flattened before passed on to the agent.
+
+    If no features are selected, then this model becomes a VariableModel, e.g. it is a variable of size nOutput.
+    """
+
+    def __init__(self, nOutput : int, state_size : int = 0, config : Config = None, *, kwargs_cfg : dict = None, **kwargs ):
+        """
+        Create standard Agent.
+
+        The model implements a dense network of 'depth' and 'width' with activation function 'activation'.
+        The final layer then condenses the last 'width' nodes to 'nOutput' nodes, usually with a linear 'final_act'.
+        The model will extract the user-requested features from the 'data' dictionary provided to __call__.
+        The user specifies the desired features with the 'features' config keyword. The model can be made to always
+        use some features by using 'required_features'.
+
+        The model can initialize the model with zero initial value, but with non-trivial initial gradients.
+        It does this by returning the difference between two networks, with the same initial weights, but where only
+        the first is trainable.
+
+        If the model is created without features it will represent a VariableModel.
+
         Parameters
         ----------
-            gym : Gym
-                Instance of a gym derived from Gym.
-                Note that in case the gym is restored from the cache this object is replaced via set_gym().
-            tf_trn_data : dict
-                Dictionary of TF data to be passed to the gym during training.
-                If the sample path are distributed according to some sample_weights,
-                then this dictionary must contain the probabiltiy weights and key_sample_weights must
-                be set to the name of this element.
-            tf_val_data : dict
-                Dictionary of TF data used for validation. Set to None for no validation
-            trn_sample_weights : np.ndarray
-                Sample weights for the training data set. None for the uniform distribution.
-            val_sample_weights : np.ndarray
-                Sample weights for the validation data set. None for the uniform distribution.
-            key_loss : str
-                Name of the primary loss vector returned from a gym predict call.
-                The environment will use thise to extract the current loss.
-                This is used for determining the best loss (with the training data).
-            **kwargs : 
-                Other arguments to be passed to 'self', see PrettyDict.
-                In particular, this allows assigning member values to the environment as follows:
-                
-                    e = Environment(gym, trn_data, user_data = user_data )
-                    
-                in this case  'user_data' is available in the environment in all subsequent contexts                
-        """
-        _log.verify( not gym is None, "'gym' cannot be None")
-        _log.verify( isinstance(gym, Gym), "'gym' must be derived from 'Gym'. Found type '%s'", type(gym).__name__)
-        _log.verify( isinstance( tf_trn_data, Mapping), "tf_trn_data must be a Mapping. Found type '%s'", type(tf_trn_data).__name__ if not tf_trn_data is None else "None")
-        _log.verify( key_loss != "", "'key_loss' cannot be an empty string")
-        if not tf_val_data is None: _log.verify( isinstance( tf_val_data, Mapping), "tf_val_data must be a Mapping. Found type '%s'", type(tf_val_data).__name__)
-        
-        self.gym                = gym
-        self.key_loss           = str(key_loss)
-        self.trn                = PrettyDict()
-        self.trn.tf_data        = tfCast( tf_trn_data )
-        self.trn.sample_weights = np.asarray( trn_sample_weights ) if not trn_sample_weights is None else None
-        if not self.trn.sample_weights is None:
-            self.trn.sample_weights = self.trn.sample_weights[:,0] if len(self.trn.sample_weights) == 2 and self.trn.sample_weights.shape[1] == 1 else self.trn.sample_weights
-            _log.verify( len(self.trn.sample_weights.shape) == 1, "'trn_sample_weights' must be a vector or of shape (N,) or (N,1), but found tensor of shape %s", trn_sample_weights.shape)
+            nOutput :
+                number of output states
+            state_size :
+                If non-zero, this specifies the second dimension of an additional state vector which is to be passed
+                to the agent when calling() it.
+                This allows the calling user to add a fixed state to the otherwise dynamic features extracted during
+                runtime
+
+            kwargs_cfg, **kwargs:
+                Only one of these can be non-empty.
+                They are both used to drive the configuration of the underlying network.
+                The general principle for each parameter is the same, and allows the developer to (a) set a default value for each
+                setting, and (b) either fix the setting or let the user set it using a 'config' object.
+                Example: 'depth'
+
+                    def_depth       : defines the default depth for the network to be created. This default is set by the developer.
+                    depth           : if set, then depth is fixed by the developer to this number. The user cannot overwrite this.
+                    config('depth') : if kwargs contains a 'config' element, and if 'depth' is not set, then the function will
+                                      read 'depth' from the config as specified to the user.
+
+                The settings thus controlled are:
+                    width        : width of the network. Default is 50
+                    depth        : depth, default 3
+                    activation   : activation function in core network, default 'relu'
+                    final_activation : activation function to compress last 'width' to nOutput. Usually left to its default 'linear'.
+                    zero_model   : whether the model is initialzed to zero initial value (but not zero gradients), default True.
+                                   Practically, the model constructs both the original model F and a non-trainable
+                                   model F', then sets the weights of F' to the initial weights of F, and defines
+                                   the full model as M=F-F'. If 'trainable' is False then this function returnbs a network
+                                   with zero initial value.
+                    regression   : hard set the network to a pure regression model. This is a debugging option with default False.
+                                   This is equivalent to setting depth = 0, width = nInput, and final_activation = 'linear'.
+
+                A more complex example is that of selecting features for the underlying agent.
+                Those are specified by name. The agent will then drive extraction of the relevant data from the data universe automatically.
+
+                    def_features     : just as in the above example, these are the default features for the agent.
+                    required_features: features which the agent always needs to use
+                    allow_no_features: whether or not to allow an empty list fo features. This is set to False if required_features
+
+                    features         : if specified by the developer, then these features are always used.
+                                       Note that if required_features are defined, then the two lists are merged.
+
+                    config('features') : if 'features' is not specified, then the user may choose her own features.
+
+                Finally, both kwargs_cfg and kwargs may also contain standard keyword parameters for tf.keras.Model() such as dtype, name, trainable.
+        """
+        assert kwargs_cfg is None or len(kwargs) == 0, "Cannot specify 'kwargs_cfg' and **kwargs"
+
+        kwargs                   = to_config(kwargs_cfg if not kwargs_cfg is None else kwargs, config_name="kwargs_DenseAgent")
+        nOutput                  = int(nOutput)
+        state_size               = int(state_size)
+        _log.verify( nOutput > 0, "'nOutput' must be positive. Found %ld", nOutput )
+        _log.verify( state_size >= 0, "'state_size' must not be negative. Found %ld", state_size )
+
+        dtype                    = kwargs('dtype', def_dtype )
+        name                     = kwargs('name', None, (str, None))
+        trainable                = kwargs('trainable', True, bool)
+        tf.keras.Model.__init__(self, name=name, dtype=dtype, trainable=trainable )
+
+        self._model              = None
+        self._available_features = None
+        self._size_features      = None
+        self._nOutput            = nOutput
+        self._state_size         = state_size
+
+        self._features           = kwargs('features', None, (None, list))
+        def_features             = kwargs("def_features", [], list)
+        req_features             = kwargs("required_features", [], list)
+        allow_no_features        = kwargs("allow_no_features", True, bool) if len(req_features)==0 else False
+        self._kwargs             = kwargs.detach() # store kwargs for a subsequent call to dense_model()
+
+        config                   = config if not config is None else Config()
+        self._features           = config("features", def_features, list, "Names of features to be used by this agent") if self._features is None else self._features
+        self._features           = list(set( self._features + req_features ))
+        self._config             = config.detach() # store config for a subsequent call to dense_model()
+        self._features.sort()
+        _log.verify( len(self._features) > 0 or allow_no_features, "'features' cannot be left empty")
+        config.done() # catch user errors
+        kwargs.done() # catch dev errors
+
+    # ----------------------------
+    # keras build/call
+    # ----------------------------
+
+    def build(self, shapes_data_and_state : dict ):
+        """ Extract the requested features from the shapes provided """
+        assert self._model is None, "'build' called twice?"
+
+        state_shape = shapes_data_and_state.get('state', None)
+        shapes      = shapes_data_and_state['data']
+
+        self._available_features = list(shapes.keys())
+        self._available_features.sort()
+
+        self._size_features = 0
+        missing         = []
+        for f in self._features:
+            fs = shapes.get(f,None)
+            if fs is None:
+                missing.append(f)
+                continue
+            # we will flatten all features
+            if len(fs) > 2:
+                fs = [ fs[0], np.product( fs.as_list()[1:] ) ]
+            self._size_features += fs[1] if len(fs) > 0 else 1
+
+        if len(missing) > 0:
+            missing   = fmt_list(missing)
+            available = fmt_list(self._available_features, "(none)")
+            _log.throw("Could not extract the following features: %s. Available features are: %s", missing, available)
+
+        self._model = dense_model(
+                nInput      = self._size_features + self._state_size,
+                nOutput     = self._nOutput,
+                config      = self._config,
+                kwargs_cfg  = self._kwargs
+                )
 
-        if tf_val_data is None:
-            self.val = None
+    def call(self, data_with_state : dict, training : bool = False) ->  tf.Tensor:
+        """
+        Return action based on data provied
+        This construction here is a bit convoluted. Would prefer to just use __call__ TODO
+        """
+        assert not self._model is None, "build() was not called...?"
+        data     = data_with_state['data']
+        state    = data_with_state['state'] if self._state_size > 0 else None
+        features = None
+        if len(self._features) > 0:
+            features  = [ data[f] for f in self._features ]
+            features  = [ tf_make_dim( f, target_dim=2 ) for f in features ]
+            features  = tf.concat( features, axis=1 ) if len(features) > 1 else features[0]
+            assert features.shape[1] == self._size_features, "Internal error: %ld != %ld" % ( features.shape[1], self._size_features)
+
+        if self._state_size > 0:
+            _log.verify( not state is None, "Error calling '%s': state_size was set to %ld, hence you need to provide a state. Found 'None'")
+            _log.verify( len(state.shape) == 2 and int(state.shape[1]) == self._state_size, "Error calling '%s': state_size was set to %ld, hence you need to provide a state of shape [None, %ld]. Found tensor of shape %s", self._state_size, self._state_size, state.shape.as_list())
+            features = tf.concat( [features, state], axis=1) if not features is None else state
         else:
-            self.val                = PrettyDict()
-            self.val.tf_data        = tfCast( tf_val_data )
-            self.val.sample_weights = np.asarray( val_sample_weights ) if not val_sample_weights is None else None
-            _log.verify( self.trn.sample_weights is None == self.val.sample_weights is None, "'val_sample_weights' and 'trn_sample_weights' must be specified jointly, or jointly omitted")
-
-            if not self.val.sample_weights is None:
-                self.val.sample_weights = self.val.sample_weights[:,0] if len(self.val.sample_weights) == 2 and self.val.sample_weights.shape[1] == 1 else self.val.sample_weights
-                _log.verify( len(self.trn.sample_weights.shape) == 1, "'val_sample_weights' must be a vector or of shape (N,) or (N,1), but found tensor of shape %s", val_sample_weights.shape)
-
-        if len(kwargs) > 0:
-            self.update(kwargs)
-            
-    def set_gyml(self, gym : Gym, cached : bool ):
-        """
-        Called to set the gym of the environment.
-        This function can be overwritten to handle additional process with the gym
-        
+            _log.verify( state is None, "Error calling '%s': model is not recurrent, but a state was provided. Set state to 'None'.", name(self) )
+
+        assert features is None or isinstance( features, tf.Tensor ), "'features' must be a tensor, not %s" % type(features).__name__
+        return self._model( features if not features is None else data, training=training )
+
+    def __call__(self, data : dict, state : tf.Tensor = None, **kwargs ):
+        """
+        Compute agent result.
+
+
         Parameters
         ----------
-            gym : Model
-                The gym
-            cached : bool
-                Indicates whether the gym has been restored from disk
-        """
-        _log.verify( isinstance( gym, Gym ), "Cannot call set_model(): gym must be derived from Gym. Found type '%s'", type(gym).__name__ if not gym is None else "None" )
-        self.gym = gym
-        
-    def predict(self):
-        """
-        Call current gym on tf_data and tf_val_data to predict the latest results of the gym
-        
+            data : dict
+                Dictionary containing the models' named features for this model. Does not include 'state'
+            state : tf.Tensor or None
+                If the model has a state, then 'state' must be set to a matrix tensor with second dimension equal to self.size_recurrent_state.
+                For the first call, this is the initial state. For subsequent calls, provide the 'new_state' of the previous __call__()
+                If the model does not have a state, then 'state' must be None
+            **kwargs:
+                see tf.keras.Model.__call__()
+
         Returns
         -------
-            A PrettyDict which contains
-                trn.result : numpy arrays of the training results from gym(trn.tf_data)
-                trn.loss   : float of the training loss for the current gym               
-            If val is not None:
-                val.result : numpy arrays of the validation results from gym(val.tf_data)
-                val.loss   : float of the validation loss for the current gym               
-        """
-        # training set
-        pack              = PrettyDict()
-        pack.trn          = PrettyDict()        
-        pack.trn.results  = npCast( self.gym(self.trn.tf_data) )
-        _log.verify( isinstance(pack.trn.results, np.ndarray) or ( isinstance(pack.trn.results, Mapping) and self.key_loss in pack.trn.results), "The data returned from the gym must either be the loss tensor, or be a dictionary with '%s' entry as specified by 'loss_key'. Model returned data type %s", self.key_loss, str(type(pack.trn.results)))
-
-        pack.trn.loss     = pack.trn.results if isinstance(pack.trn.results, np.ndarray) else pack.trn.results[self.key_loss]
-        pack.trn.loss     = pack.trn.loss[:,0] if len(pack.trn.loss.shape) == 2 and pack.trn.loss.shape[1] == 1 else pack.trn.loss
-        _log.verify( len(pack.trn.loss.shape) == 1, "'loss' must be a vector or of shape (N,1). Found tensor of shape %s", pack.trn.loss.shape)
-        if not self.trn.sample_weights is None:
-            _log.verify( len(pack.trn.loss) == len(self.trn.sample_weights), "Invalid training sample weight vector: loss vector returned by gym is of length %ld, while training sample weights are of length %ld", len(pack.trn.loss), len(self.trn.sample_weights))        
-        pack.trn.loss    = np.sum( self.trn.sample_weights * pack.trn.loss ) if not self.trn.sample_weights is None else np.mean( pack.trn.loss )     
-
-        # validation set        
-        if self.val is None:
-            pack.val = None
+            A tuple (result, new_state)
+            If the model has a state, then 'new_state' is the state to be passed to the next function call.
+            If the model does not have a state, then 'state' is None
+        """
+        assert isinstance( data, Mapping ), "'data' must be dictionary or similar, not '%s'" % type(data).__name__
+        if self._state_size > 0:
+            _log.verify( isinstance( state, tf.Tensor ), "'state' must be tensor of shape [None, %ld], not a type '%s'", self._state_size, type(state).__name__ )
         else:
-            pack.val          = PrettyDict()
-            pack.val.results  = npCast( gym(tf_val_data) ) 
-            pack.val.loss     = pack.val.results if isinstance(pack.val.results, np.ndarray) else pack.val.results[self.key_loss]
-            pack.val.loss     = pack.val.loss[:,0] if len(pack.val.loss.shape) == 2 and pack.val.loss.shape[1] == 1 else pack.val.loss
-            pack.val.loss     = np.sum( self.val.sample_weights * pack.val.loss ) if not self.val.sample_weights is None else np.mean( pack.val.loss )     
-
-        return pack
-        
-# ==========================================================================
-# ProgressData
-# Base class for relevant data to be computed during training for user
-# feedback (e.g. history of losses; current state of the gym)
-# ==========================================================================
+            _log.verify( state is None, "'state' must be None, not '%s'", type(state).__name__  )
+        return tf.keras.Model.__call__(self, dict( data=data, state=state ) if not state is None else dict(data=data), **kwargs )
+
+    # ----------------------------
+    # data access
+    # ----------------------------
+
+    @property
+    def features(self) -> list:
+        """
+        Returns the features used by this agent
+        Agent needs to have been called at least once
+        """
+        assert not self._model is None, "agent model needs to be called at least once before calling this function"
+        return self._features
+
+    @property
+    def size_features(self) -> int:
+        """ Returns the size of the featues of this agent """
+        return self._size_features
+
+    @property
+    def has_features(self) -> bool:
+        """ Whether the agent has any features """
+        return len(self._features) > 0
+
+    @property
+    def available_features(self) -> list:
+        """
+        Returns the sorted list of available features for this agent.
+        Agent needs to have been called at least once
+        """
+        assert not self._model is None, "agent model needs to be called at least once before calling this function"
+        return self._available_features
+
+    @property
+    def num_output(self) -> int:
+        """ Returns the dimnension of the action output tensor """
+        return self._nOutput
+
+    @property
+    def num_trainable_weights(self) -> int:
+        """
+        Returns the number of weights. The gym must have been call()ed once
+        Agent needs to have been called at least once
+        """
+        assert not self._model is None, "agent model needs to be called at least once before calling this function"
+        weights = self.trainable_weights
+        return np.sum( [ np.prod( w.get_shape() ) for w in weights ] ) if not weights is None else 0.
+
+    @property
+    def has_state(self):
+        """ Whether this agent is recurrent """
+        return self._state_size > 0
 
-class ProgressData(object):
+    @property
+    def state_size(self):
+        """ Returns the size of the recurrent state """
+        return self._state_size
+
+    @property
+    def dim_all_features(self) -> int:
+        """
+        Returns the size of the total features vector after flattening
+        Agent needs to have been called at least once
+        """
+        assert not self._model is None, "agent model needs to be called at least once before calling this function"
+        return self._size_features
+
+class RecurrentAgent(tf.keras.Model):
     """
-    Base class for relevant data to be computed during training for user
-    feedback (e.g. history of losses; current state of the gym).
-    
-    This class is intended to be derived from, and that you overwrite on_epoch_end.
-    
-    For being used in Ray, this class needs to be pickle'able.
+    Recurrent agent
+
+    The recurrence framework for the Deep Hedging pattern is explicit - it requires the user to explicitly handle states as part of the data sets
+    used doing training in the 'gym' framework.
+
+    The core pattern is as follows:
+
+    def build(self, shapes):
+        self.agent          = RecurrentAgent(...)
+
+    def call(self, data, training=False):
+
+        features_time_0 = data(...)
+        state           = agent.initial_state(features_time_0)
+        for t in range(nSteps):
+            features_t    = data(...)
+            action, state = self.agent( features_t, state=state, training=training )
+            ....
+
+    See discussion in RecurrentAgent.__init__() for further details.
     """
-    
-    STOP_CONVERGED   = -1
-    STOP_ABORTED     = -2
-    CONTINUE         = 0
-    
-    def __init__(self, environment     : Environment,        # gym, tf_data, etc
-                       training_info   : TrainingInfo,       # total number of epochs requested etc
-                       predicted_data0 : PrettyDict         
-                       ):
-        """
-        Initialize the cachable progress data store
-        ** Do not store the gym or the training data into this object **
-        
+
+    def __init__(self, nOutput : int, config : Config = None, init_config : Config = None, *, init_kwargs : dict = None, main_kwargs : dict = None, **kwargs ):
+        """
+        Create recurrent Agent.
+
+        This model implements a recurrent agent with LSTM-like recurent nodes.
+
+        Let s' be the previous state and N be the network. Let f be the current feature set.
+        Then
+
+            a
+            r = N( s', f )
+            g
+
+        where 'a' is the new action, 'g' is the gate and 'r' is the new candidate state.
+        Let
+
+            c = sigmoid(g)
+
+        and set the new state to:
+
+            s' := c * r' + (1-c) s
+
+        The network N itself is constructed with the same method as an Agent, e.g. it is a dense network with specified
+        activation function, depth, and width, and a final, usually linear, layer.
+
+        The model will extract the user-requested features from the 'data' dictionary provided to __call__.
+        The user specifies the desired features with the 'features' config keyword. The model can be made to always
+        use some features by using 'required_features'.
+
+        Important
+        ---------
+        The model's __call__() function expects that the current state is provided.
+        In addition, __call__() returns not a single tensor, but the tuple of the main result and the new state to be used in the next logical call.
+        See __call__()
+
         Parameters
         ----------
-            environment : Environment,
-                provides access to various non-serializable objects in the training loop
-            epochs : int
-                Number of epochs to be computed.
-            predicted_data0 : PrettyDict
-                Result of environment.predict(). If None, this will be computed on-the-fly.
-                
-        """
-        self.times_per_epoch = []
-        self.trn_losses      = [ predicted_data0.trn.loss ]
-        self.val_losses      = [ predicted_data0.val.loss ] if not predicted_data0.val is None else None
-        
-        # best epoch
-        self.best_epoch      = -1
-        self.best_weights    = environment.gym.get_weights()
-        self.best_loss       = predicted_data0.trn.loss
-    
-    @property
-    def current_epoch(self):
-        """ Returns the current epoch. Returns -1 if no epoch was yet recorded """
-        return len(self.times_per_epoch)-1
-    
-    def on_epoch_end(self,  environment    : Environment,  # gym, tf_data, etc
-                            predicted_data : PrettyDict,   # current predicted training and validation data; current loss.
-                            training_info  : TrainingInfo, # number of epochs to be computed etc
-                            logs           : dict          # logs c.f. keras Callback
-                        ) -> int:
-        """ 
-        Callback at the end of an epoch. Typically used to update visuals.
-        Return self.STOP_CONVERGED or self.STOP_ABORTED to abort training or self.CONTINUE to continue
-        """
-        return self.CONTINUE
-    
-    def on_done(self,       environment    : Environment,  # gym, tf_data, etc
-                            predicted_data : PrettyDict,   # current predicted training and validation data; current loss.
-                            training_info  : TrainingInfo, # number of epochs to be computed etc
-                        ):
-        """
-        Called when training is finished and the gym was set to the best weights
-        Typically used to update any visualization and print a summary.
-        """
-        pass
-        
-    # --------------------
-    # Internal
-    # --------------------
-            
-    def _on_epoch_end(self, environment    : Environment,  # gym, tf_data, etc
-                            training_info  : TrainingInfo, # number of epochs to be computed etc
-                            time_epoch     : float,        # time required for 
-                            logs           : dict          # logs c.f. keras Callback
-                        ):
-        """
-        Called at the end of an epoch by Callback()
-        Will store the time for the epoch in 'times_per_epoch'
-        
-        This function is called by the training loop.
-        Do not overwrite this function; instead overwrite on_epoch_end()
-        """
-        assert len(self.times_per_epoch)+1 == len(self.trn_losses), "Internal error: %ld+1 != %ld" % (len(self.times_per_epoch), len(self.trn_losses))
-
-        predicted_data = environment.predict()
-
-        self.times_per_epoch.append( time_epoch )
-        self.trn_losses.append( predicted_data.trn.loss )
-        if not self.val_losses is None:
-            self.val_losses.append( predicted_data.val.loss )
-        
-        if self.best_loss > predicted_data.trn.loss:
-            self.best_epoch   = self.current_epoch
-            self.best_weights = environment.gym.get_weights()
-            self.besr_loss    = predicted_data.trn.loss
-        
-        return self.on_epoch_end( environment=environment, predicted_data=predicted_data, training_info=training_info, logs=logs )
-        
-    def _on_done(self,      environment    : Environment,  # gym, tf_data, etc
-                            training_info  : TrainingInfo, # number of epochs to be computed etc
-                        ):
-        """ 
-        Called by the Callback() when training is done, after the best weights have been written to the gym.
-        Do not overwrite this function; overwrite on_done()
-        """
-        predicted_data = environment.predict()
-        self.on_done( environment=environment, predicted_data=predicted_data, training_info=training_info )
-        
-    def _write_best( self,  gym : Gym ):
-        """ Write best weights to the gym, if any """
-        if self.best_epoch >= 0:
-            gym.set_weights( self.best_weights )
-        
-# ==========================================================================
-# Callback
-# This is called during training to handle caching and user updates
-# ==========================================================================
+            nOutput :
+                number of outputs.
+
+            config : Config
+                User-driven configuration for this agent.
+                Main fields are:
+                        'init'          :  network specification for the initial agent
+                        'recurrence'    : number of recurrent nodes
+                        Rest is sent to DenseAgent()
+
+            kwargs:
+                You can only specify kwargs or init_kwargs and main_kwargs.
+                If kwargs is specified, then all its keys starting with 'init_' will be moved to init_kwargs, with the remainder copied to main_kwargs.
+
+            init_kwargs:
+                Keywords which drive the initialization of the initial state for the recurrent network.
+                Typically, the initial state
+                    - has a less deep network, e.g. with smaller depths and width.
+                    - only uses features which are meaningful at time 0, e.g. exclude keys such as 'time_left' in deep hedging.
+                The keywords available are described in DenseAgent.__init__()
+
+            main_kwargs:
+                Keywords which drive the configuration of the main agent network.
+                Most keywords available are described in DenseAgent.__init__().
+
+                In addition:
+                    recurrence       : If specified, sets the number of recurrent states for this network. In this case 'recurrence' cannot be set by the user.
+                    def_recurrence   : sets the default number of recurrent states for this network. The default is 5.
+        """
+        assert (init_kwargs is None and main_kwargs is None) or len(kwargs) == 0, "Cannot specify 'init_kwargs', 'main_kwargs' and **kwargs"
+
+        init_kwargs = to_config( { k[5:] : kwargs[k] for k in kwargs if k[:5] == "init_" } if init_kwargs is None else init_kwargs, config_name="kwargs_Recurrent_init" )
+        main_kwargs = to_config( { k     : kwargs[k] for k in kwargs if k[:5] != "init_" } if main_kwargs is None else main_kwargs, config_name="kwargs_Recurrent_main" )
+
+        dtype                    = main_kwargs('dtype', def_dtype )
+        name                     = main_kwargs('name', None, (str, None))
+        trainable                = main_kwargs('trainable', True, bool)
+        init_kwargs['dtype']     = dtype
+        init_kwargs['name']      = name if name is None else (name + "_init")
+        init_kwargs['trainable'] = trainable
+
+        tf.keras.Model.__init__(self, name=name, dtype=dtype, trainable=trainable )
+
+        self._nOutput     = int(nOutput)
+        assert self._nOutput > 0, "Ouput must be positive, not %ld" % nOutput
+
+        recurrence       = main_kwargs('recurrence', None, (None, Int>=0))
+        def_recurrence   = main_kwargs('def_recurrence', 5, Int>=0)
+
+        # handle main recurrence
+        config           = config if not config is None else Config()
+        self._recurrence = config("recurrence", def_recurrence, Int>=0, "Number of recurrent nodes") if recurrence is None else recurrence
+        config_init      = init_config if not init_config is None else Config()
+        config_main      = config
+
+        self._main_agent  = DenseAgent( nOutput=self._nOutput+2*self._recurrence, state_size=self._recurrence, config=config_main, kwargs_cfg=main_kwargs )
+        self._init_agent  = DenseAgent( nOutput=self._nOutput+self._recurrence, config=config_init, kwargs_cfg=init_kwargs )
+        init_kwargs.done() # catch misspelled keywords, and catches remaining config() items
+        main_kwargs.done() # catch misspelled keywords, and catches remaining config() items
+
+    # ----------------------------
+    # Execution
+    # ----------------------------
+
+    def initial_action_and_state(self, features : dict, **kwargs ) -> tuple:
+        """
+        Return the value of the initial action and state.
+        """
+        assert isinstance( features, Mapping ), "'features' must be dictionary or similar"
+        r      = self._init_agent( features, **kwargs )
+        if self._recurrence == 0:
+            return r, None
+        n      = self._recurrence
+        state  = r[:,:n]
+        action = r[:,n:]
+        return action, state
+
+    def __call__(self, features : dict, state : tf.Tensor, **kwargs ) -> tuple:
+        """
+        Compute recurrent action and state
+
+        This function accepts a dictionary of generic named features, and a dedicated state.
+        The state variable should be initialized with the initial state returned by
+        self.initial_agent_and_state() at the beginning of the recurrent sequence.
 
-class Callback(tf.keras.callbacks.Callback):
-    """
-    Manages training of our gym    
-    -- Keeps track of training data in TrainingProgressData including best fit
-    -- Implements caching
-    -- Implements dyanmic visual updates
-    """
-    
-    STOP_ABORTED     = ProgressData.STOP_ABORTED
-    STOP_CONVERGED   = ProgressData.STOP_CONVERGED
-    CONTINUE         = ProgressData.CONTINUE
-    STOP_INTERRUPTED = -10
-    FINISHED_EPOCHS  = 1
-    ALREADY_TRAINED  = 2
-    
-    def __init__(self, *, environment    : Environment,
-                          training_info  : TrainingInfo,
-                          progress_data  : progress_data,
-                          cache_config   : PrettyDict,
-                          verbose        : Context = Context() ):
-        """
-        Initialize the call back
-        The object will attempt to restore a previous training state from disk if found.
-        
         Parameters
         ----------
-            model_cachable
-                Model derived from Model.
-            epochs : int
-                Total number of epochs for this training. If the cached object has been trained beyond that point, no further training will commence.
-            default_cache_directory : str
-                Default caching directory for 
-        """
-        
-        tf.keras.callbacks.Callback.__init__(self)
-        
-        gym                  = environment.gym
-        _log.verify( isinstance(gym, Gym), "'gym' must be derived from 'Gym'")
-
-        # basics
-        self.environment      = environment
-        self.training_info    = training_info
-        self.progress_data    = progress_data
-        self.cache_last_epoch = progress_data.current_epoch
-        self.verbose          = verbose
-        self.time_start       = time.time()
-        self.stop_reason      = self.CONTINUE
-        _log.verify( self.training_info.epochs > 0, "'epochs' must be positive. Found %ld", self.training_info.epochs )
-        assert not self.is_done, "Internal error: nothing to train?"
-        
-        # caching
-        self.cache_mode       = cache_config.cache_mode
-        self.cache_freq       = cache_config.cache_freq
-        self.cache_dir        = cache_config.cache_dir
-        self.time0            = time.time()
-
-    def write_cache(self):
-        """ Write cache to disk """
-        if self.cache_last_epoch >= self.progress_data.current_epoch:
-            assert self.cache_last_epoch == self.progress_data.current_epoch, "Interal error: %ld > %ld ?", (self.cache_last_epoch, self.progress_data.current_epoch)
-            return
-        assert self.progress_data.current_epoch >= 0, "Internal error: current epoch is -1"
-        self.cache_dir.write( PROGRESS_FILE, self.progess_data )
-        self.environment.gym.save( self.cache_dir + MODEL_FILE )
-        self.cache_last_epoch = self.progress_data.current_epoch
-        
-    @property
-    def is_done(self):
-        """ Checks whether training has finished. This can happen at inception if a cache is restored which was trained for as many epochs as requested """
-        return self.progress_data.current_epoch+1 >= self.training_info.epochs
-    
-    @property
-    def current_epoch(self):
-        """ Returns the current epoch. -1 if no epoch was run """
-        return self.progress_data.current_epoch
-    
-    @property
-    def epochs(self):
-        return self.training_info.epochs
-
-    def on_epoch_begin( self, loop_epoch, logs = None ):#NOQA
-        pass
-    
-    def on_epoch_end( self, loop_epoch, logs = None ):
-        """
-        Called when an epoch ends
-        Will call prorgress_data.on_epoch_end()
-        
-        Note that 'loop_epoch' is the epoch of the current training run.
-        If the state was recovered from a cache, it won't be the logical epoch
-        """
-
-        time_now = time.time()
-        _current = self.progress_data.current_epoch
-        r = self.progress_data._on_epoch_end( environment   = self.environment,
-                                              training_info = self.training_info,
-                                              time_epoch    = time_now - self.time_start,
-                                              logs          = logs )
-        assert self.progress_data.current_epoch >= 0, "Internal error: progress_data must update its epoch count"
-        assert self.progress_data.current_epoch > _current, ("Internal error: progress_data must update its epoch count", self.progress_data.current_epoch, _current)
-
-        # allow calling progress data to abort training
-        if r in [ProgressData.STOP_ABORTED, ProgressData.STOP_CONVERGED]:
-            self.write_cache()
-            self.stop_reason         = r
-            self.gym.stop_training = True
-
-        self.time_start = time_now
-        
-        if self.current_epoch % self.cache_freq == 0 and self.cache_mode.write and self.progress_data.current_epoch > self.cache_last_epoch:
-            self.write_cache()
-            
-    def finalize( self ):
-        """
-        Close training. Call this even if training was aborted
-        -- Cache the current state
-        -- Apply best weight
-        """
-        # cache current state /before/ we reset gym to its best weights
-        # this way we can continue to train from where we left it
-        cached_msg = ""
-        if self.progress_data.current_epoch >= 0 and self.cache_mode.write:
-            self.write_cache()
-            cached_msg = " State of training until epoch %ld cached into %s\n" % (self.cache_last_epoch+1, self.full_cache_file)
-            
-        status = ""
-        if self.stop_reason == self.STOP_ABORTED:
-            status = "Training aborted"
-        elif self.stop_reason == self.STOP_CONVERGED:
-            status = "Desired convergence achieved"
-        elif self.stop_reason == self.STOP_INTERRUPTED:
-            status = "User abort"
-        elif self.stop_reason == self.FINISHED_EPOCHS:
-            status = "Trained %ld epochs" % self.epochs
-        elif self.stop_reason == self.ALREADY_TRAINED:
-            status = "Model was already trained for at least %ld epochs" % self.epochs
-        else:
-            _log.throw("Unknown stopping reason %ld", self.stop_reason)            
+            features :
+                Dictionary of features
+            state :
+                Tensor which represents the current state of the recurrent agent.
+                For the first step, initialize the state with initial_state().
+            **kwargs:
+                passed to the underlying model call
 
-        # restore best weights & tell user
-        self.progress_data._write_best( self.environment.gym )
-        self.progress_data._on_done(  environment   = self.environment,
-                                      training_info = self.training_info )
-        
-        self.verbose.write( "Status: %(status)s.\n"\
-                           " Weights set to best epoch: %(best_epoch)ld\n"\
-                           "%(cached_msg)s Time: %(time)s",\
-                           status=status, 
-                           best_epoch=self.progress_data.best_epoch+1,
-                           cached_msg=cached_msg,
-                           time=fmt_now())
-
-# ==========================================================================
-# Main training loop
-# ==========================================================================
-
-@tf.function
-def default_loss( y_true,y_pred ):     
-    """ Default loss: ignore y_true """
-    return y_pred
-
-def train(   environment    : Environment,
-             create_progress: type = ProgressData,
-             config         : Config = Config(),
-             verbose        : Context = Context() ):
-    """
-    Main training loop
-    
-    Parameters
-    ----------
-        environment : Environment
-            Contains the (initial) gym, training and validation data sets. Also contains sample weights.
-            You can provide a derived class if you wish to pass on further information to progess_data.on_epoch_end
-            Alternatively, you can pass a dictionary with the required elements to construct an Environment object
-            Note: if a gym is loaded back from disk, then environment.set_gym() is called.
-        progress_data : ProgressData
-            Main callback: the function on_epoch_end() is called at the end of each epoch.
-            This function is then intended to compute all other summary statistics required for user feedback doing training.
-            The object needs to be pickle'abel if it is intended to be used a multiprocessing environment such as Ray
-        config : Config
-            Standard config
-        verbose :
-            Controls level of output.
+        Returns
+        -------
+            This function returns (action, state)
+        """
+        assert isinstance( features, Mapping ), "'features' must be dictionary or similar"
+        if self._recurrence == 0:
+            _log.verify( state is None, "Model '%s' is not recurrent, hence 'state' must None", name(self))
+            return self._main_agent( features, **kwargs ), None
+
+        _log.verify( not state is None, "Model '%s': 'state' cannot be 'None'. Use initial_state()", name(self))
+        _log.verify( len(state.shape) == 2 and int(state.shape[1]) == self._recurrence, "Model '%s': state is expected to be of shape [None, %ld]. Found shape %s", name(self), self._recurrence, state.shape.as_list())
+        result    = self._main_agent( features, state=state, **kwargs )
+        n         = self._recurrence
+        new_state = result[:,0*n:1*n]
+        gate      = result[:,1*n:2*n]
+        action    = result[:,2*n:]
+        assert action.shape[1] == self._nOutput, "Internal error: %ld != %ld" % (action.shape[1], self._nOutput)
+        gate      = tf.math.sigmoid( gate )
+        state     = state * gate + (1. - gate) * new_state
+        return action, state
 
-    Returns
-    -------
-        A PrettyDict which contains, computed at the best weights:
-            gym           : trained gym, set to best weights (according to training data)
-                            Note that this object may differ from the original environment.gym if it was restored from a cache
-            progress_data : progress data, e.g. a version of ProgressData which contains at the very least the time series of losses, and the best weights
-            trn.result    : numpy arrays of the training results from gym(trn.tf_data)
-            trn.loss      : float of the training loss for the current gym               
-        If val is not None:
-            val.result    : numpy arrays of the validation results from gym(val.tf_data)
-            val.loss      : float of the validation loss for the current gym               
-    """
-    verbose.write("Initializing training")
-    
-    # --------------------
-    # Prep & Caching
-    # --------------------
-        
-    # how much to print
-    debug_numerics   = config.debug("check_numerics", False, bool, "Whether to check TF numerics.")
-    tf_verbose       = config.debug("tf_verbose", 0, Int>=0, "Verbosity for TensorFlow fit()")
-    
-    # training parameters    
-    batch_size       = config.train("batch_size",  None, help="Batch size")
-    epochs           = config.train("epochs",      100, Int>0, help="Epochs")
-    run_eagerly      = config.train("run_eagerly", False, help="Keras gym run_eagerly. Turn to True for debugging. This slows down training. Use None for default.")
-    tboard_log_dir   = config.train.tensor_board(   "log_dir", "", str, "Specify tensor board log directory. See https://www.tensorflow.org/guide/profiler")
-    tboard_freq      = config.train.tensor_board(   "hist_freq", 1, Int>0, "Specify tensor board log frequency. See https://www.tensorflow.org/guide/profiler") 
-    tboard_prf_batch = config.train.tensor_board(   "profile_batch", 0, help="Batch used for profiling. Set to non-zero to activate profiling. See https://www.tensorflow.org/guide/profiler") 
-
-    # create gym  
-    # In the current design the newly created gym is replaced by the restored gym if found
-    gym                      = environment.gym
-    optimizer_uid            = config.train.optimizer.unique_id()
-    train_uid                = uniqueFileName48( [ gym.cache_uid(), optimizer_uid, gym.CACHE_VERSION ] )
-    
-    # caching
-    def_directory_name       = gym.cache_def_directory_name + "/batch_size_" + (str(batch_size) if not batch_size is None else "default")
-    cache_config             = pdct()
-    cache_config.cache_mode  = config.caching("mode", CacheMode.ON, CacheMode.MODES, "Caching strategy: %s" % CacheMode.HELP)
-    cache_config.cache_freq  = config.caching("epoch_freq", 10, Int>0, "How often to cache results, in number of epochs")
-    cache_dir                = config.caching("directory", "./.cache/" + gym.cache_def_directory_name, str, "Caching directory")
-    cache_file_name          = config.caching("file_name", "", str, "Allows overwriting the filename for debugging an explicit cached state")
-    config.done()
-
-    cache_file               = train_uid if cache_file_name == "" else cache_file_name
-    cache_dir                = SubDir( cache_dir, "!" )
-    cache_config.cache_dir   = cache_config.cache_dir.subdir( cache_file )
-    cache_config.cache_mode  = CacheMode( cache_config.cache_mode )
-
-    training_info = TrainingInfo( batch_size     = batch_size,
-                                  epochs         = epochs)
-
-    # --------------------
-    # Restore cache
-    # --------------------
-    
-    progress_data            = cache_config.cache_dir.read( PROGRESS_FILE, None )
-    if not progress_data is None:
-        """ Handle cached gym """
-        assert not progress_data.cache_last_epoch is None
-        assert progress_data.cache_last_epoch <= progress_data.current_epoch, (progress_data.cache_last_epoch, progress_data.current_epoch
-        config.progress.mark_done()
-        config.train.optimizer.mark_done()
-                                                                               
-        gym  = keras.models.load_model( cache_config.cache_dir.path + MODEL_FILE  )
-        epochs = epochs - (progress_data.current_epoch+1)
-        verbose.report(1, "Loaded gym from cache %s. Model was trained for %ld epochs.", cache_config.cache_dir.path, progress_data.current_epoch )
-        environment.set_model( gym, cached=True )
-        
-        if epochs <= 0:
-            config.done()
-            progress_data._write_best(environment.gym)
-            verbose.write("Finished training as cached gym is fully trained")
-            result               = environment.predict()
-            result.progress_data = progress_data
-            result.gym           = gym            
-            return result
-        
-        verbose.report(1, "Preparing training for the remaining %ld epochs", epochs )
-    else:
-        """ No gym cached yet """
-        verbose.report(1, "Model generated. Preparing training for %ld epochs", epochs )
-        gym.compile(    optimizer        = create_optimizer(config.train.optimizer),
-                        loss             = { environment.key_loss : default_loss },
-                        weighted_metrics = { environment.key_loss : default_loss },
-                        run_eagerly      = run_eagerly)
-        environment.set_model( gym, cached=False )
- 
-        progress_data = create_progress( environment=environment,
-                                         training_info=training_info,
-                                         config=config.progress )
-        
-    config.done()
-    
-    # --------------------
-    # Training
-    # --------------------
-    
-    t0             = time.time()
-    pack0          = environment.predict()
-    verbose.write("Model has %ld trainable weights." % gym.num_trainable_weights)    
-    callback       = Callback(    environment     = environment,
-                                  training_info   = training_info,
-                                  create_progress = create_progress,
-                                  config          = config,
-                                  verbose         = verbose.sub(1) )
-    config.done()
-
-    # train
-    # -----
-    
-    if debug_numerics:
-        tf.debugging.enable_check_numerics()
-        verbose.report(1, "Enabled automated checking for numerical errors. This will slow down training. Use config.debug.check_numerics = False to turn this off")
-    else:
-        tf.debugging.disable_check_numerics()
-    
-    if not callback.is_done:
-        assert epochs > (callback.current_epoch+1), "Internal error. callback.is_done failed"
-        # tensorboard
-        # See https://docs.aws.amazon.com/sagemaker/latest/dg/studio-tensorboard.html
-
-        tboard = None
-        if tboard_log_dir != "":
-            t0             = time.time()
-            tboard_log_dir = SubDir(tboard_log_dir).path
-            tboard         = tf.keras.callbacks.TensorBoard(log_dir=tboard_log_dir, histogram_freq=tboard_freq, profile_batch=tboard_prf_batch )
-            verbose.report(1,"TensorBoard log directory set to '%s'. Took %s" % (tboard_log_dir, fmt_seconds(time.time()-t0)))
-
-        def find_sample_size( x ):
-            if isinstance(x, tf.Tensor):
-                assert int(x.shape[0])>0, x.shape
-                return int(x.shape[0])
-            if isinstance(x, dict):
-                for x in x.values():
-                    l = find_sample_size(x)
-                    if l>0:
-                        return l
-            else:
-                _log.verify( isinstance(x, list), "Cannot determine data sample size for type %s", str(type(x)))
-                for x in x:
-                    l = find_sample_size(x)
-                    if l>0:
-                        return l
-            return 0
-        
-        nSamples = find_sample_size(environment.trn.tf_data)
-        _log.verify( nSamples > 0, "Cannot determine data sample size: no tensors found")
-        y        = tf.zeros((nSamples,), dtype=gym.dtype)
-
-        try:
-            gym.fit(        x              = environment.trn.tf_data,
-                            y              = y,
-                            batch_size     = batch_size,
-                            sample_weight  = environment.trn.sample_weights * float(len(environment.trn.sample_weights)) if not environment.trn.sample_weights is None else None,  # sample_weights are poorly handled in TF
-                            epochs         = epochs - (callback.current_epoch+1),
-                            callbacks      = callback if tboard is None else [ callback, tboard ],
-                            verbose        = tf_verbose )
-            callback.stop_reason = Callback.FINISHED_EPOCHS            
-        except KeyboardInterrupt:
-            callback.stop_reason = Callback.STOP_INTERRUPTED
-
-    callback.finalize()
-    verbose.report(0, "Training completed. Total training took %s", fmt_seconds(time.time()-t0))
-    result = environment.predict()
-    result.progress_data = callback.progress_data
-    result.gym = gym
-    return result
+    # ----------------------------
+    # syntatic sugar
+    # ----------------------------
+
+    @property
+    def has_features(self) -> bool:
+        """ Whether the agent has any features """
+        return self._init_agent.has_features
+
+    @property
+    def has_state(self) -> bool:
+        """ Whether this agent has an initial state """
+        return self._recurrence > 0
+
+    @property
+    def num_trainable_weights(self) -> int:
+        """
+        Returns the number of weights. The gym must have been call()ed once
+        Agent needs to have been called at least once
+        """
+        weights = self.trainable_weights
+        return np.sum( [ np.prod( w.get_shape() ) for w in weights ] ) if not weights is None else 0.
 
+    @property
+    def is_recurrent(self) -> bool:
+        """ Whether the agent is recurrent """
+        return self._recurrence > 0
 
+    @property
+    def recurrence(self) -> int:
+        """ Number of recurrent states. """
+        return self._recurrence
 
+    @property
+    def init_agent(self) -> DenseAgent:
+        """ Returns the DenseAgent used for the initial state. Returns None if agent is not recurrent"""
+        return self._init_agent
+
+    @property
+    def main_agent(self) -> DenseAgent:
+        """ Returns the DenseAgent used for the main (loop) action """
+        return self._main_agent
```

### Comparing `cdx_tf-0.1.1/cdx_tf/optimizer.py` & `cdx_tf-0.1.2/cdx_tf/optimizer.py`

 * *Files 4% similar despite different names*

```diff
@@ -3,41 +3,40 @@
 ------------------
 Import this file in all deep hedging files.
 June 30, 2022
 @author: hansbuehler
 """
 
 from cdxbasics.logger import Logger
-from cdxbasics.config import Confiog
-from .util import tf
+from cdxbasics.config import Config, Float, Int#NOQA
+from .util import tf, TF_VERSION
 import inspect as inspect
 _log = Logger(__file__)
 
 def create_optimizer( config : Config ):
     """
     Creates an optimizer from a config object
     The keywords accepted are those documented for https://www.tensorflow.org/api_docs/python/tf/keras/optimizers
-    
+
     You can use:
         config.optimizer = "adam"
         config.optimizer = tf.keras.optimizers.Adam(learning_rate = 0.01)
-    """    
+    """
     if isinstance( config, str ):
         return tf.keras.optimizers.get(config)
 
     # new version. Specify optimizer.name
-    config    = config.optimizer
     name      = config("name", "adam", str, "Optimizer name. See https://www.tensorflow.org/api_docs/python/tf/keras/optimizers")
 
     # auto-detect valid parameters
     optimizer = tf.keras.optimizers.get(name)
     sig_opt   = inspect.signature(optimizer.__init__)
     classname = optimizer.__class__
     kwargs    = {}
-    
+
     # all parameters requested by the optimizer class
     for para in sig_opt.parameters:
         if para in ['self','name','kwargs']:
             continue
         default = sig_opt.parameters[para].default
         if default == inspect.Parameter.empty:
             # mandatory parameter
@@ -56,12 +55,12 @@
                         ema_momentum=0.99,
                         ema_overwrite_frequency=None)
     for k in hard_coded:
         if k in kwargs:
             continue  # handled already
         v = hard_coded[k]
         kwargs[k] = config(k, v, help="Parameter %s for keras optimizers" % k)
-    
+
     config.done()
     return optimizer.__class__(**kwargs)
```

### Comparing `cdx_tf-0.1.1/cdx_tf/util.py` & `cdx_tf-0.1.2/cdx_tf/util.py`

 * *Files 25% similar despite different names*

```diff
@@ -9,14 +9,16 @@
 from cdxbasics.logger import Logger
 from cdxbasics.util import isAtomic
 import numpy as np
 import tensorflow as tf
 import math as math
 import inspect as inspect
 import datetime as datetime
+from collections.abc import Mapping, Collection
+
 _log = Logger(__file__)
 
 # -------------------------------------------------
 # Manage tensor flow
 # -------------------------------------------------
 
 TF_VERSION = [ int(x) for x in tf.__version__.split(".") ]
@@ -34,27 +36,27 @@
 Each world data dictionary must have an element with this name, whcih needs to be of dimension (None,1)
 This is used in layers.VariableLayer in order to scale the variable up to the number of samples
 
 The reason the dimension is (None,1) and not (None,) is that older Tensorflow versions auto-upscale data
 of dimension (None,) to (None,1) anyway.
 
 It's not a pretty construction but there seems to be no other nice way in TF to find our current sample size.
-"""                                
+"""
+
+DIM_DUMMY = "_dimension_dummy"
 
-DIM_DUMMY = "_dimension_dummy"  
-        
 # -------------------------------------------------
 # TF <--> NP
 # -------------------------------------------------
 
 def tfCast( x, native = True, dtype=def_dtype ):
     """
     Casts an object or a collection of objecyts iteratively into tensors.
     Turns all custom dictionaries (such as PrettyDict) into dictionaries unless 'native' is False.
-    
+
     Parameters
     ----------
         x
             object. Can be list of lists of dicts of numpys etc
                 - numpy arrays become tenors
                 - tensors will be cast to dtype, if required
                 - atomic variables become tensor constants
@@ -62,58 +64,58 @@
         native : bool, optional
             True
                 - lists-types of x's becomes lists of tensors
                 - dicts-types of x's becomes dicts of tensors
             False:
                 - lists-types of x's stay list-types
                 - dicts-types of x's stay dict-types
-                            
+
         dtype : tf.DType, optional
             Overwrite dtype
-            
+
     Returns
     -------
         tensors.
     """
     if x is None:
         return None
     if isinstance(x, tf.Tensor):
         return x if ( dtype is None or x.dtype == dtype ) else tf.convert_to_tensor( x, dtype=dtype )
     if isinstance(x, np.ndarray):
         return tf.convert_to_tensor( x, dtype=dtype )
     if isAtomic(x):
-        return tf.constant( x, dtype=dtype )     
+        return tf.constant( x, dtype=dtype )
     if isinstance(x, dict):
         d = { _ : tfCast(x[_], dtype=dtype) for _ in x }
         return d if native or (type(x) == 'dict') else x.__class__(d)
     if isinstance(x, list):
-        l = [ tfCast(x[_], dtype=dtype) for _ in x ]
+        l = [ tfCast(_, dtype=dtype) for _ in x ]
         return l if native or (type(l) == 'list') else x.__class__(l)
-    
+
     _log.verify( False, "Cannot convert object of type '%s' to tensor", x.__class__.__name__)
     return None
 
 def npCast( x, dtype=None ):
     """
     Casts an object or a collection of objecyts iteratively into numpy arrays.
-    
+
     Parameters
     ----------
         x
             object. Can be list of lists of dicts of tensors etc
                 - tensors become numpy arrays (copies !)
                 - numpy arrays will be cast into dtype if necessaryt
                 - atomic variables become arrays with shape ()
                 - lists of x's becomes lists of npCast(x)'s
                 - dicts of x's becomes dicts of npCast(x)'s
                 - None returns None
-            
+
         dtype : tf.DType, optional
             Overwrite dtype
-            
+
     Returns
     -------
         numpys.
     """
     if x is None:
         return None
     if isinstance(x, tf.Tensor):
@@ -122,139 +124,171 @@
         return np.asarray( x, dtype=dtype )
     if isAtomic(x):
         return np.array(x, dtype=dtype )
     if isinstance(x, dict):
         d  = { _ : npCast(x[_], dtype=dtype) for _ in x }
         return d if type(x) == 'dict' else x.__class__(d)
     if isinstance(x, list):
-        l = [ npCast(x[_], dtype=dtype) for _ in x ]
+        l = [ npCast(_, dtype=dtype) for _ in x ]
         return l if type(l) == 'list' else x.__class__(l)
-    
+
     return  np.asarray( x, dtype=dtype )
 
+def tf_dict( dtype=None, **kwargs ):
+    """ Return a (standard) dictionary of tensors """
+    return tfCast(kwargs, dtype=dtype)
+
+# -------------------------------------------------
+# Loss
+# -------------------------------------------------
+
+def get_sample_size( data : dict, raise_error : bool = True ) -> tf.Tensor:
+    """
+    Extract the current sample size from a 'data' dictionary as it is usually passed to
+    tf.keras.layers.Layer.__call__ or tf.kersas.Model.__call__
+
+    Parameters
+    ----------
+        data : dict or tensor
+            Read batch sample size from this object
+        raise_error : bool
+            If True, an exception is rasied in case no tensor could be found
+    Returns
+    -------
+        Returns first dimension of the first tensor this function finds a tensor, or 0.
+        Note that this function may return None if the current sample size is not set yet, for example
+        in
+    """
+    if isinstance(data, tf.Tensor):
+        assert data.shape[0] is None or int(data.shape[0])>0, data.shape
+        return int(data.shape[0]) if not data.shape[0] is None else None
+    if isinstance(data, Mapping):
+        for x in data.values():
+            l = get_sample_size(x)
+            if l>0:
+                return l
+    else:
+        _log.verify( isinstance(data, Collection), "Cannot determine data sample size for type %s", str(type(x)))
+        for x in data:
+            l = get_sample_size(x)
+            if l>0:
+                return l
+    _log.verify( not raise_error, "Cannot determine sample size: no tensors found in 'data'")
+    return 0
+
+# -------------------------------------------------
+# Loss
+# -------------------------------------------------
+
+@tf.function(reduce_retracing=True)
+def default_loss( y_true,y_pred ):
+    """ Default loss: ignore y_true """
+    return y_pred
+
 # -------------------------------------------------
 # TF flattening
 # -------------------------------------------------
 
-@tf.function
+if False:
+    # below code seems more natural, but does not work with None dimensions
+    def tf_make_dim( tensor : tf.Tensor, target_dim : int = 2, name : str = None ) -> tf.Tensor:
+        """
+        Ensure a tensor as a given dimension by either flattening at the end to
+        reduce diemnsions, or adding tf.newaxis to increase them.
+
+        x = tf.Tensor( np.array((16,8,4,2)) )
+        tf_back_flatten( x, dim = 1)   --> shape [16*8*4*2]
+        tf_back_flatten( x, dim = 2)   --> shape [16,8*4*2]
+        x = tf.Tensor( np.array((16,)) )
+        tf_back_flatten( x, dim = 2)   --> shape [16,1]
+
+        Parameters
+        ----------
+            tensor : tf.Tensor
+                A tensor
+            target_dim : int
+                target dimension of the flattened tensor.
+            name : str
+                Name or None. Name will not be set if the current shape of the tensor matches 'target_dim'
+
+        Returns
+        -------
+            Tensor of dimension 'target_dim'
+        """
+        target_dim = int(target_dim)
+        _log.verify( target_dim > 0, "'target_dim' most be positive")
+        dim        = len(tensor.shape)
+
+        if dim > target_dim:
+            target_shape = [ int(tensor.shape[i]) if tensor.shape[i] is None else None for i in range(target_dim) ]
+            target_shape[target_dim-1] = np.prod( [ int(i) for i in tensor.shape[target_dim-1:] ] )
+            tensor       = tf.reshape( tensor, tuple(target_shape), name=name )
+        elif dim < target_dim:
+            target_shape = [ int(i) if not i is None else None for i in tensor.shape ]
+            target_shape += [1] * ( target_dim - len(tensor.shape) )
+            tensor       = tf.reshape( tensor, tuple(target_shape), name=name )
+
+        return tensor
+
 def tf_back_flatten( tensor : tf.Tensor, target_dim : int = 2) -> tf.Tensor:
     """
     Flattens a tensor while keeping the first 'dim'-1 axis the same.
-    
+
     x = tf.Tensor( np.array((16,8,4,2)) )
     tf_back_flatten( x, dim = 1)   --> shape [16*8*4*2]
     tf_back_flatten( x, dim = 2)   --> shape [16,8*4*2]
     ...
-    
+
     Use case: assume we are given features for an ML model.
     First dimension is number of Samples. Subsequent dimensions might be present, but are not relevant for network construction.
     This function allows flattening it such that the first dimension remains the number of samples, while the rest is flattened.
-    
+
     Use tf_make_dim to also handles whose existing dimension is less than target_dim
-        
+
     Parameters
     ----------
         tensor : tf.Tensor
             A tensor
         target_dim : int
             max dimension of the flattened tensor.
-            
+
     Returns
     -------
         Flat tensor.
     """
-    _log.verify( target_dim > 0 and target_dim <= len(tensor.shape), "'target_dim' most be positive and not exceed dimension of tensor, %ld. Found target_dim %ld. If this intended, use 'tf_make_dim' instead", len(tensor.shape), target_dim)     
+    _log.verify( target_dim > 0 and target_dim <= len(tensor.shape), "'target_dim' most be positive and not exceed dimension of tensor, %ld. Found target_dim %ld. If this intended, use 'tf_make_dim' instead", len(tensor.shape), target_dim)
     if len(tensor.shape) > target_dim:
-        splits = [ tf_back_flatten( tensor[...,_], dim=target_dim ) for _ in range(tensor.shape[-1]) ]
-        tensor = tf.concat( splits, axis=-1 )    
+        splits = [ tf_back_flatten( tensor[...,_], target_dim=target_dim ) for _ in range(tensor.shape[-1]) ]
+        tensor = tf.concat( splits, axis=-1 )
     return tensor
 
-@tf.function
 def tf_make_dim( tensor : tf.Tensor, target_dim : int = 2) -> tf.Tensor:
     """
     Ensure a tensor as a given dimension by either flattening at the end to
     reduce diemnsions, or adding tf.newaxis to increase them.
-    
+
     x = tf.Tensor( np.array((16,8,4,2)) )
     tf_back_flatten( x, dim = 1)   --> shape [16*8*4*2]
     tf_back_flatten( x, dim = 2)   --> shape [16,8*4*2]
-
     x = tf.Tensor( np.array((16,)) )
     tf_back_flatten( x, dim = 2)   --> shape [16,1]
-    
+
     Parameters
     ----------
         tensor : tf.Tensor
             A tensor
         target_dim : int
             target dimension of the flattened tensor.
-            
+
     Returns
     -------
         Flat tensor.
     """
     try:
         if len(tensor.shape) > target_dim:
             return tf_back_flatten(tensor,target_dim)
         while len(tensor.shape) < target_dim:
             tensor = tensor[...,tf.newaxis]
         return tensor
     except AttributeError as e:
         _log.throw( "Error converting tensor to dimension %ld: %s\nTensor is %s of type %s", target_dim, e, str(tensor), type(tensor) )
 
-# -------------------------------------------------
-#  Object management
-# -------------------------------------------------
-
-def create_optimizer( config : Config ):
-    """
-    Creates an optimizer from a config object
-    The keywords accepted are those documented for https://www.tensorflow.org/api_docs/python/tf/keras/optimizers
-    
-    You can use:
-        config.optimizer = "adam"
-        config.optimizer = tf.keras.optimizers.Adam(learning_rate = 0.01)
-    """    
-    if isinstance( config, str ):
-        return tf.keras.optimizers.get(config)
-
-    # new version. Specify optimizer.name
-    config    = config.optimizer
-    name      = config("name", "adam", str, "Optimizer name. See https://www.tensorflow.org/api_docs/python/tf/keras/optimizers")
-
-    # auto-detect valid parameters
-    optimizer = tf.keras.optimizers.get(name)
-    sig_opt   = inspect.signature(optimizer.__init__)
-    classname = optimizer.__class__
-    kwargs    = {}
-    
-    # all parameters requested by the optimizer class
-    for para in sig_opt.parameters:
-        if para in ['self','name','kwargs']:
-            continue
-        default = sig_opt.parameters[para].default
-        if default == inspect.Parameter.empty:
-            # mandatory parameter
-            kwargs[para] = config(para, help="Parameter %s for %s" % (para,classname))
-        else:
-            # optional parameter
-            kwargs[para] = config(para, default, help="Parameter %s for %s" % (para,classname))
-
-    # The following parameters are understood by general tensorflow optimziers
-    hard_coded = dict(  clipnorm=None,
-                        clipvalue=None,
-                        global_clipnorm=None )
-    if TF_VERSION >= 211:
-        hard_coded.update(
-                        use_ema=False,
-                        ema_momentum=0.99,
-                        ema_overwrite_frequency=None)
-    for k in hard_coded:
-        if k in kwargs:
-            continue  # handled already
-        v = hard_coded[k]
-        kwargs[k] = config(k, v, help="Parameter %s for keras optimizers" % k)
-    
-    config.done()
-    return optimizer.__class__(**kwargs)
-
-
```

