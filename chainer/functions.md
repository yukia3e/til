# What is __functions__
Chainer provides basic _Function_ implementations in the _chainer.functions_ package.  
Most of them are wrapped by plain Python functions, which users should use.  


# How to use it
```python
from chainer import functions as F
```


# fucntions
## matmul
Computes the matrix multiplication of two arrays.  

```python
F.matmul(a, b, transa=False, transb=False)
# Parameters:
# a (Variable) - The left operand of the matrix multiplication. A 1-D array of shape `(N,)` is considered as an N×1 matrix. A 2-D array of shape `(M, N)` is considered as an M×N matrix.
# b (Variable) - The right operand of the matrix multiplication. Its array is treated as a matrix in the same way as `a`‘s array.
# transa (bool) - If `True`, transpose `a`.
# transb (bool) - If `True`, transpose `b`.
# Return:
# Variable - The result of the matrix multiplication as a 2-D array.
```


## transpose
Permute the dimensions of an input variable without copy.  

```python
F.transpose(x, axes=None)
# Parameters:
# x (Variable) – Input variable.
# axes (tuple of ints) – By default, reverse the dimensions, otherwise permute the axes according to the values given.
# Return:
# Variable - Variable whose axes are permuted.
```


## split_axis
Splits given variables along an axis.  

```python
F.split_axis(x, indices_or_sections, axis, force_tuple=False)
# Parameters:
# x (tuple of Variables) – Variables to be split.
# indices_or_sections (int or 1-D array) – If this argument is an integer, N, the array will be divided into N equal arrays along axis. If it is a 1-D array of sorted integers, it indicates the positions where the array is split.
# axis (int) – Axis that the input array is split along.
# force_tuple (bool) – If True, this method returns a tuple even when the number of outputs is one.
# Return:
# tuple of Variable - Tuple of Variable objects if the number of outputs is more than 1 or Variable otherwise. When force_tuple is True, returned value is always a tuple regardless of the number of outputs.
```


## softplus
Elementwise softplus function.  
This function is expressed as $f(x) = \frac{1}{\beta}log(1+exp(\beta x))$, where $\beta$ is parameter.  

```python
F.softplus(x, beta=1.0)
# Parameters:
# x (Variable) – Input variable.
# beta (float) – Parameter beta.
# Return:
# Variable - Output variable.
```


## batch_12_norm_squared
Computes the inverse of a batch of square matrices.

```python
F.batch_12_norm_squared(a)
# Parameters:
# a (Variable) – Input array to compute the inverse for. Shape of the array should be (m, n, n) where m is the number of matrices in the batch, and n is the dimensionality of a square matrix.
# Return:
# Variable - Inverse of every matrix in the batch of matrices.
```
