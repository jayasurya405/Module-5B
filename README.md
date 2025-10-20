# NumPy Program: Column-wise Sorting of a 2D Array

## 🎯 Aim
To write a NumPy program that sorts the elements in each column of a given 2D array in ascending order.

## 🧠 Algorithm
Import NumPy: Start by importing the NumPy library.
Get Input: Accept a 2D NumPy array from the user.
Sort Column-wise: Use the np.sort() function with axis=0 to sort each column in ascending order.
Store Result: Store the sorted result in a new array.
Display Output: Print the original array and the column-wise sorted array.

## 🧾 Program
```
import numpy as np

# Example 2D NumPy array
arr = np.array([[10, 6,9],
                [9, 5, 4],
                [4, 8, 3]])

# Sort each column in ascending order using axis=0
sorted_arr = np.sort(arr, axis=0)

print("Original array:")
print(arr)
print("\nColumn-wise sorted array:")
print(sorted_arr)
```
## Output
<img width="1131" height="887" alt="Screenshot 2025-10-20 220805" src="https://github.com/user-attachments/assets/7084e0f8-8c37-4622-a937-fb79da7779e0" />


## Result
Thus To write a NumPy program that sorts the elements in each column of a given 2D array in ascending order has been executed sucessfully.

# NumPy Program: Find Indices Where Elements in Array x are Greater Than or Equal to Corresponding Elements in Array y

## 🎯 Aim
To write a Python program using NumPy that finds the indices where elements in array x are greater than or equal to their corresponding elements in array y.

## 🧠 Algorithm
Import NumPy: Import the NumPy library.
Define Arrays: Define two NumPy arrays, x and y, with the same shape (i.e., same number of elements).
Use Boolean Indexing:
x > y gives a boolean array where elements of x are greater than y.
x == y gives a boolean array where elements of x are equal to y.
Find Indices: Use np.where() to get the indices where the conditions x >= y are satisfied.
Print Indices: Print the indices where the condition holds true.

## Program
```
import numpy as np

# Define two arrays x and y of the same shape
x = np.array([1, 3, 5, 7, 9])
y = np.array([2, 3, 4, 8, 7])

# Find indices where elements in x are greater than or equal to elements in y
indices = np.where(x >= y)

print("Indices where x >= y:", indices[0])
```  
## Output
<img width="1045" height="886" alt="Screenshot 2025-10-20 221101" src="https://github.com/user-attachments/assets/99cc5944-d0cd-4130-808c-1c27f250bc90" />


## Result
Thus To write a Python program using NumPy that finds the indices where elements in array x are greater than or equal to their corresponding elements in array y has been executed sucessfully.

# NumPy Program: Replace the Second Column in a 2D Array

## 🎯 Aim
To write a NumPy program that deletes the second column from a given 2D array and inserts a new column at the same position.

## 🧠 Algorithm
Import NumPy: Start by importing the NumPy library.
Get Input: Get a 2D NumPy array and a new column (as another array) from the user.
Delete Column: Use np.delete() to remove the second column (index 1) from the original array.
Insert Column: Use np.insert() to insert the new column at the second column's original position.
Display Result: Print the updated array with the replaced column.

## 🧾 Program
```
import numpy as np

# Example original 2D array
arr = np.array([[1, 2, 3],
                [4, 5, 6],
                [7, 8, 9]])

# Example new column to insert
new_col = np.array([10, 11, 12])

# Delete the second column (index 1)
arr_deleted = np.delete(arr, 1, axis=1)

# Insert the new column at index 1
arr_updated = np.insert(arr_deleted, 1, new_col, axis=1)

print("Original array:")
print(arr)
print("\nUpdated array after replacing second column:")
print(arr_updated)
```
## Output
<img width="1137" height="915" alt="Screenshot 2025-10-20 221251" src="https://github.com/user-attachments/assets/80d7cd1c-420f-4a20-86c6-3c38cfe3fbc3" />


## Result
Thus To write a NumPy program that deletes the second column from a given 2D array and inserts a new column at the same position has been executed sucessfully.

# Pandas Program: Create and Display a DataFrame with Custom Index Labels

## 🎯 Aim
To create and display a DataFrame using the Pandas library in Python from a given dictionary, and apply specific index labels to the rows.

## 🧠 Algorithm
Import Libraries: Import the required libraries – pandas and numpy.
Create Dictionary: Define a dictionary exam_data with keys: 'name', 'score', 'attempts', and 'qualify'.
Index Labels: Create a list of custom index labels called labels.
Create DataFrame: Use pd.DataFrame() to create the DataFrame by passing the dictionary and index labels.
Display Output: Display the DataFrame using print() or by simply calling the DataFrame variable.

## 💻 Program
```
import pandas as pd
import numpy as np

# Define the input dictionary
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}

# Define custom index labels
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']

# Create DataFrame with custom index
df = pd.DataFrame(exam_data, index=labels)

# Display DataFrame
print(df)
```
## Output
<img width="1152" height="905" alt="Screenshot 2025-10-20 221418" src="https://github.com/user-attachments/assets/62783a30-6f11-463a-8f15-08611294f66d" />


## Result
Thus To create and display a DataFrame using the Pandas library in Python from a given dictionary, and apply specific index labels to the rows has been executed sucessfully.

# 🧪 Pandas Program: Join Two DataFrames Along Rows

## 🎯 AIM
To write a Python program using Pandas to join two DataFrames along rows (row-wise concatenation) and assign all data to a new DataFrame.

## 🧠 ALGORITHM
Import Libraries: Import the pandas library.
Create First DataFrame: Use a dictionary to create student_data1.
Create Second DataFrame: Use another dictionary to create student_data2.
Concatenate DataFrames: Use pd.concat() with axis=0 to concatenate both DataFrames row-wise.
Display Result: Print the new combined DataFrame.

## 💻 Program
```
import pandas as pd

# Create first DataFrame
student_data1 = {
    'name': ['Alice', 'Bob', 'Charlie'],
    'age': [24, 27, 22],
    'grade': ['A', 'B', 'C']
}
df1 = pd.DataFrame(student_data1)

# Create second DataFrame
student_data2 = {
    'name': ['David', 'Eva', 'Frank'],
    'age': [23, 26, 28],
    'grade': ['B', 'A', 'C']
}
df2 = pd.DataFrame(student_data2)

# Concatenate DataFrames row-wise (along axis=0)
combined_df = pd.concat([df1, df2], axis=0)

# Display the combined DataFrame
print(combined_df)
```
## Output
<img width="819" height="914" alt="Screenshot 2025-10-20 221534" src="https://github.com/user-attachments/assets/1da81502-b6e1-401f-b813-a151661e89d9" />


## Result
Thus To write a Python program using Pandas to join two DataFrames along rows (row-wise concatenation) and assign all data to a new DataFrame has been executed sucessfully.
