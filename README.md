# Python-Data-Science-and-Machine-Learning-Bootcamp
Repo for Python Data Science and Machine Learning Bootcamp

# Personal notes

# Numpy arrays (Vectores and Matrices)

np.arange(start, finish, step)
Example: np.arange(0,10,2) => array([0,2,4,6,8,9])

np.linspace(start, finish, n_of_steps)
Example: np.linspace(0, 5, 9) => array([0, 0.625, 1.25 , 1.875,2.5  , 3.125, 3.75 , 4.375, 5])

`np.zeros(rows, columns)` => matrix of zeros
`np.ones(rows, columns)` => matrix of ones

np.eye(rows, columns) => Identity matrix

- Random numbers
np.random.rand(rows) => One-dimensional array of 5 random numbers between 0 and 1 with uniform distribution
np.random.randn(rows, columns (optional)) => One or two dimensional arrau of 5 random numbers with standard normal (gaussian) distribution
np.random.randint(low, high, amount) => Returns ramndom int between low and high(non-inclusive) range. Thirud optional argument to return array of random ints in that range.

arr.reshape(rows,columns) => Returns data of an array arranged with the specific number of rows and columns. Has to match the amount of elements.
For example:
`arr = np.arrange(0,16)` // [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15]
`arr.reshape(4,4)` // [[0,1,2,3], [4,5,6,7], [8,9,10,11], [12,13,14,15]]

- Max and min values
`arr.max()` / `arr.min()` => Max / Min value of array
`arr.argmax()` / `arr.argmin()` => Index of max / min value

* Array slices
Numpy arrays are different than python arrays because they're able to broadcast, or setting values with index ranges. In numpy arrays, when you slice an array and set it to a variable, you're referencing the same array in memory, not a new one. For example:
`arr = np.arange(0,100)`
`arr2 = arr[:10]`

To copy, you need to specify:
`arr2 = arr[:10].copy()`

* Indexing of matrices (2d arrays)
We can do double bracker format: arr[1][2]
or single bracket format: arr[1, 2]

We can do matrix slicing, for example:
arr2d = arr[:2, :1] // This would grab until row 2, and columns until 1 (not included)

* Fancy indexing: We can select whole rows in any order
arr2d = [[9, 4, 6, 8]]  // This will select rows 9, 4, 6 and 8 and return them as a matrix in that order.

* Applying operations to arrays
`arr = array([3,4,5,6,7])`
`bool_arr = arr > 5` // [False, False, False, True, True]

- Conditional selection
`arr[bool_arr]` // [6,7]

Or more concise:
arr[arr > 5] // arr > 5 creates a boolean array map that can be used to index the original array, like a filter.

* numpy operations

Array addition, multiplication, division, substraction (not concat)
`arr = [1, 2, 3]`
`arr + arr` // [2, 4, 6]

Scalar operations
arr + 1 // [2, 3, 4]

Universal array functions -> Math operations that broadcast through all elements of an array. For example:
`np.sqrt(arr)` / makes the square root of all elements of array
`np.sin(arr)` / np.log(arr)

# PANDAS

Pandas series are like hashes / dictionaries. We can pass any data structure into them (list, dictionary, numpy array, function) and it will store them in order, with number index (key) by default.

`my_data = [10,20,30]`
`pd.Series(data=my_data)`

0    10
1    20
2    30
dtype: int64

We can also specify on the second argument `index=`the keys by which we will reference the data

`labels = ['a', 'b', 'c']`
`pd.Series(data=my_data, index=labels)`

a    10
b    20
c    30
dtype: int64
