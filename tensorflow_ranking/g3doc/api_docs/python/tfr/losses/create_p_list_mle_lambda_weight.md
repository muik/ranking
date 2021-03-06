<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tfr.losses.create_p_list_mle_lambda_weight" />
<meta itemprop="path" content="Stable" />
</div>

# tfr.losses.create_p_list_mle_lambda_weight

<!-- Insert buttons -->

<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/ranking/tree/master/tensorflow_ranking/python/losses.py">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>

<!-- Start diff -->

Creates _LambdaWeight based on Position-Aware ListMLE paper.

```python
tfr.losses.create_p_list_mle_lambda_weight(list_size)
```

<!-- Placeholder for "Used in" -->

Produces a weight based on the formulation presented in the "Position-Aware
ListMLE" paper (Lan et al.) and available using
create_p_list_mle_lambda_weight() factory function above.

#### Args:

*   <b>`list_size`</b>: Size of the input list.

#### Returns:

A _LambdaWeight for Position-Aware ListMLE.
