<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tfr.feature.encode_listwise_features" />
<meta itemprop="path" content="Stable" />
</div>

# tfr.feature.encode_listwise_features

<!-- Insert buttons -->

<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/ranking/tree/master/tensorflow_ranking/python/feature.py">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>

<!-- Start diff -->

Returns dense tensors from features using feature columns.

```python
tfr.feature.encode_listwise_features(
    features,
    context_feature_columns,
    example_feature_columns,
    input_size=None,
    mode=tf.estimator.ModeKeys.TRAIN,
    scope=None
)
```

<!-- Placeholder for "Used in" -->

#### Args:

*   <b>`features`</b>: (dict) mapping feature names (str) to feature values
    (`tf.Tensor` or `tf.SparseTensor`), possibly obtained from input_fn. For
    context features, the tensors are 2-D, while for example features the
    tensors are 3-D.
*   <b>`context_feature_columns`</b>: (dict) context feature names to columns.
*   <b>`example_feature_columns`</b>: (dict) example feature names to columns.
*   <b>`input_size`</b>: (int) [DEPRECATED: Use without this argument.] number
    of examples per query. If this is None, input_size is inferred as the size
    of second dimension of the Tensor corresponding to one of the example
    feature columns.
*   <b>`mode`</b>: (`estimator.ModeKeys`) Specifies if this is training,
    evaluation or inference. See `ModeKeys`.
*   <b>`scope`</b>: (str) variable scope for the per column input layers.

#### Returns:

*   <b>`context_features`</b>: (dict) A mapping from context feature names to
    dense 2-D tensors of shape [batch_size, ...].
*   <b>`example_features`</b>: (dict) A mapping frome example feature names to
    dense 3-D tensors of shape [batch_size, input_size, ...].

#### Raises:

*   <b>`ValueError`</b>: If `input size` is not equal to 2nd dimension of
    example tensors.
