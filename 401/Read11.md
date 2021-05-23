# Data Analysis
- JupyterLab : web based interface that enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner , supports using wide collection of programing languages , it also can handle MD in really cool and organized way

- Can open most of the pic extensions and you can use - = to zoom in and out,[] to rotate and 0 to reset,ETC

# NumPy 
- Definition : NumPy is a commonly used Python data analysis package. By using NumPy, you can speed up your workflow, and interface with other packages in the Python ecosystem

- The data is called ssv (semicolon separated values) format — each record is separated by a semicolon (;), and rows are separated by a new line.

- Lists Of Lists for CSV Data
we’ll first try to work with the data using Python and the csv package.We can read in the file using the csv.reader object, which will allow us to read in and split up all the content from the ssv file.

- Steps:
1. Import the csv library.
2. Open the winequality-red.csv file.
3. With the file open, create a new csv.reader object.
4. Pass in the keyword argument delimiter=";" to make sure that the records are split up on the semicolon character instead of the default comma character.
5. Call the list type to get all the rows from the file.
6. Assign the result to wines.
7. import csv with open('winequality-red.csv', 'r') as f: wines = list(csv.reader(f, delimiter=';'))

- The data has been read into a list of lists. Each inner list is a row from the ssv file. we’ve read in three rows, the first of which contains column headers. Each row after the header row represents a wine as the fie holds

We can find the average quality of the wines. The below code will do the following:

- Extract the last element from each row after the header row.
- Convert each extracted element to a float.
- Assign all the extracted elements to the list qualities.
- Divide the sum of all the elements in qualities by the total number of elements in qualities to the get the mean.

        qualities = [float(item[-1]) for item in wines[1:]] sum(qualities) / len(qualities)
        
        5.6360225140712945

## Numpy 2-Dimensional Arrays
- A 2-dimensional array is also known as a matrix, and is something you should be familiar with. In fact, it’s just a different way of thinking about a list of lists. A matrix has rows and columns. By specifying a row number and a column number, we’re able to extract an element from a matrix.

- In the file used, the first row is the header row, and the first column is the fixed acidity column

- In a NumPy array, the number of dimensions is called the rank, and each dimension is called an axis. So the rows are the first axis, and the columns are the second axis.

### Creating A NumPy Array
- We can create a NumPy array using the numpy.array function. If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns.

- Import the numpy package.
Pass the list of lists wines into the array function, which converts it into a NumPy array.
Exclude the header row with list slicing.
Specify the keyword argument dtype to make sure each element is converted to a float. We’ll dive more into what the dtype is later on.
import csv with open("winequality-red.csv", 'r') as f: wines = list(csv.reader(f, delimiter=";")) import numpy as np wines = np.array(wines[1:], dtype=np.float)

We can check the number of rows and columns in our data using the shape property of NumPy arrays:

        wines.shape

        (1599, 12)

Alternative NumPy Array Creation Methods
you can create an array where every element is zero. The below code will create an array with 3 rows and 4 columns, where every element is 0, using numpy.zeros:
import numpy as np empty_array = np.zeros((3,4)) empty_array

It’s useful to create an array with all zero elements in cases when you need an array of fixed size, but don’t have any values for it yet.

You can also create an array where each element is a random number using numpy.random.rand. Here’s an example:
np.random.rand(3,4)

array([[ 0.2247223 , 0.92240549, 0.14541893, 0.61731257], [ 0.00154957, 0.82342197, 0.74044906, 0.11466845], [ 0.6152478 , 0.14433138, 0.13009583, 0.22981301]])

Using NumPy To Read In Files
It’s possible to use NumPy to directly read csv or other files into arrays. We can do this using the numpy.genfromtxt function.

Use the genfromtxt function to read in the winequality-red.csv file.
Specify the keyword argument delimiter=";" so that the fields are parsed properly.
Specify the keyword argument skip_header=1 so that the header row is skipped.
wines = np.genfromtxt("winequality-red.csv", delimiter=";", skip_header=1)

Indexing NumPy Arrays
We can use array indexing to select individual elements, groups of elements, or entire rows and columns. One important thing to keep in mind is that just like Python lists, NumPy is zero-indexed, meaning that the index of the first row is 0, and the index of the first column is 0.

Let’s select the element at row 3 and column 4. In the below code, we pass in the index 2 as the row index, and the index 3 as the column index.

        wines[2,3]

        2.2999999999999998

### Slicing NumPy Arrays
If we instead want to select the first three items from the fourth column, we can do it using a colon (:). A colon indicates that we want to select all the elements from the starting index up to but not including the ending index. This is also known as a slice:

        wines[0:3,3]
        array([ 1.9, 2.6, 2.3])

We can select an entire column by specifying that we want all the elements, from the first to the last. We specify this by just using the colon (:), with no starting or ending indices.

        wines[:,3]

We selected an entire column above, but we can also extract an entire row:

        wines[3,:]

- Assigning Values To NumPy Arrays
We can also use indexing to assign values to certain elements in arrays. We can do this by assigning directly to the indexed value:

        wines[1,5] = 10

- We can do the same for slices. To overwrite an entire column, we can do this:

        wines[:,10] = 50


### Multiple Array Math
- It’s also possible to do mathematical operations between arrays. This will apply the operation to pairs of elements. For example, if we add the quality column to itself, here’s what we get:

        wines[:,11] + wines[:,11]

        array([ 10., 10., 10., ..., 12., 10., 12.])

- Let’s say we want to pick a wine that maximizes alcohol content and quality

(we want to get drunk, but we’re classy).

We’d multiply alcohol by quality, and select the wine with the highest score:

        wines[:,10] * wines[:,11]

        array([ 47., 49., 49., ..., 66., 51., 66.])

- Broadcasting
When using Operations between dimensions the trailling should be the same

- NumPy Array Methods: In addition to the common mathematical operations, NumPy also has several methods that you can use for more complex calculations on arrays. An example of this is the numpy.ndarray.sum method. This finds the sum of all the elements in an array by default:

        wines[:,11].sum()

        9012.0

- We can pass the axis keyword argument into the sum method to find sums over an axis. If we call sum across the wines matrix, and pass in axis=0, we’ll find the sums over the first axis of the array. This will give us the sum of all the values in every column.

        wines.sum(axis=0)

        array([ 13303.1 , 843.985 , 433.29 , 4059.55 , 139.859 , 25384. , 74302. , 1593.79794, 5294.47 , 1052.38 , 16666.35 , 9012. ])


### Subsetting
- One of the powerful things we can do with a Boolean array and a NumPy array is select only certain rows or columns in the NumPy array. For example, the below code will only select rows in wines where the quality is over 7:

        high_quality = wines[:,11] > 7 wines[high_quality,:][:3,:]

result:

        array([[ 7.90000000e+00, 3.50000000e-01, 4.60000000e-01, 3.60000000e+00, 7.80000000e-02, 1.50000000e+01, 3.70000000e+01, 9.97300000e-01, 3.35000000e+00, 8.60000000e-01, 1.28000000e+01, 8.00000000e+00], [ 1.03000000e+01, 3.20000000e-01, 4.50000000e-01, 6.40000000e+00, 7.30000000e-02, 5.00000000e+00, 1.30000000e+01, 9.97600000e-01, 3.23000000e+00, 8.20000000e-01, 1.26000000e+01, 8.00000000e+00], [ 5.60000000e+00, 8.50000000e-01, 5.00000000e-02, 1.40000000e+00, 4.50000000e-02, 1.20000000e+01, 8.80000000e+01, 9.92400000e-01, 3.56000000e+00, 8.20000000e-01, 1.29000000e+01, 8.00000000e+00]])

- we can look for wines with a lot of alcohol and high quality. In order to specify multiple conditions, we have to place each condition in parentheses, and separate conditions with an ampersand (&):

high_quality_and_alcohol = (wines[:,10] > 10) & (wines[:,11] > 7) wines[high_quality_and_alcohol,10:]

- Reshaping NumPy Arrays
We can change the shape of arrays while still preserving all of their elements. This often can make it easier to access array elements. The simplest reshaping is to flip the axes, so rows become columns, and vice versa. We can accomplish this with the numpy.transpose function:

        np.transpose(wines).shape

        (12, 1599)

- We can use the numpy.ravel function to turn an array into a one-dimensional representation. It will essentially flatten an array into a long sequence of values:

        wines.ravel()

        array([ 7.4 , 0.7 , 0. , ..., 0.66, 11. , 6. ])

- we can use the numpy.reshape function to reshape an array to a certain shape we specify. The below code will turn the second row of wines into a 2-dimensional array with 2 rows and 6 columns:

        wines[1,:].reshape((2,6))

### Combining NumPy Arrays
- it’s very common to combine multiple arrays into a single unified array. We can use numpy.vstack to vertically stack multiple arrays. Think of it like the second arrays’s items being added as new rows to the first array.