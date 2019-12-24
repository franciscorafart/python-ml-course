# Python-Data-Science-and-Machine-Learning-Bootcamp
Repo for Python Data Science and Machine Learning Bootcamp

# Personal notes

# Numpy arrays (Vectores and Matrices)

np.arange(start, finish, step)
Example: np.arange(0,10,2) => array([0,2,4,6,8,9])

np.linspace(start, finish, n_of_steps)
Example: np.linspace(0, 5, 9) => array([0, 0.625, 1.25 , 1.875,2.5  , 3.125, 3.75 , 4.375, 5])

np.zeros(rows, columns) => matrix of zeros
np.ones(rows, columns) => matrix of ones

np.eye(rows, columns) => Identity matrix

- Random numbers
np.random.rand(rows) => One-dimensional array of 5 random numbers between 0 and 1 with uniform distribution
np.random.randn(rows, columns (optional)) => One or two dimensional arrau of 5 random numbers with standard normal (gaussian) distribution
np.random.randint(low, high, amount) => Returns ramndom int between low and high(non-inclusive) range. Thirud optional argument to return array of random ints in that range.

arr.reshape(rows,columns) => Returns data of an array arranged with the specific number of rows and columns. Has to match the amount of elements.
For example:
arr = np.arrange(0,16) // [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15]
arr.reshape(4,4) // [[0,1,2,3], [4,5,6,7], [8,9,10,11], [12,13,14,15]]

- Max and min values
arr.max() / arr.min() => Max / Min value of array
arr.argmax() arr.argmin() => Index of max / min value
