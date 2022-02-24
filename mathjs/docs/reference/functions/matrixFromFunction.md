<!-- Note: This file is automatically generated from source code comments. Changes made in this file will be overridden. -->

# Function matrixFromFunction

Create a matrix by evaluating a generating function at each index.
The simplest overload returns a multi-dimensional array as long as `size` is an array.
Passing `size` as a Matrix or specifying a `format` will result in returning a Matrix.


## Syntax

```js
math.matrixFromFunction(size, fn)
math.matrixFromFunction(size, fn, format)
math.matrixFromFunction(size, fn, format, datatype)
math.matrixFromFunction(size, format, fn)
math.matrixFromFunction(size, format, datatype, fn)
```

### Parameters

Parameter | Type | Description
--------- | ---- | -----------
`size` | Array &#124; Matrix | The size of the matrix to be created
`fn` | function | Callback function invoked for every entry in the matrix
`format` | string | The Matrix storage format, either `'dense'` or `'sparse'`
`datatype` | string | Type of the values

### Returns

Type | Description
---- | -----------
Array &#124; Matrix | Returns the created matrix


## Examples

```js
math.matrixFromFunction([3,3], i => i[0] - i[1]) // an antisymmetric matrix
math.matrixFromFunction([100, 100], 'sparse', i => i[0] - i[1] === 1 ? 4 : 0) // a sparse subdiagonal matrix
math.matrixFromFunction([5], i => math.random()) // a random vector
```


## See also

[matrix](matrix.md),
[zeros](zeros.md)