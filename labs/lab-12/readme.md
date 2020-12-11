# Lab 12: Sorting

Welcome to CSC 211 Lab 07. Your goal for this lab will be to gain a better understanding of sorting algorithms. **Be sure to read and follow all instructions unless otherwise specified.**  Create a `lab-12.txt` document to record all of your lab answers in and implement all of your `.cpp` programs in your IDE.

1. Bubble Sort Slides [20 minutes]<br> 
2. Selection Sort Slides [20 minutes]<br> 
3. Insertion Sort [50 minutes] <br>
4. Another Look at Arrays
5. Submission [5 minutes]

# Part 1. Bubble Sort  [20 minutes]


:white_check_mark: Question 1. Considering the bubble sort algorithm we've just discussed, how many swaps are necessary to sort the following sequence? `[2, 13, 6, 9, 3, 10, 8, 1, 5, 11]`

:white_check_mark: Question 2. Implement Bubble Sort

<img src="images/fig1.png">

# Part 2. Selection Sort Slides [20 minutes]


:white_check_mark: Question 3. Considering the selection sort algorithm we've just discussed, how many swaps are necessary to sort the following sequence? `[2, 13, 6, 9, 3, 10, 8, 1, 5, 11]`

:white_check_mark: Question 4. Implement Bubble Sort

<img src="images/fig2.png">


# Part 3. Insertion Sort [50 minutes]


Consider the pseudocode below:

<img src="images/insert.jpg">

Implement this algorithm in a file named `insertionSort.cpp`.

:white_check_mark: Question 5. Is this algorithm faster than the other two? Justify your answer. <br>

# Part 4. Another Look at Arrays

Arrays are similar to lists in Python but fundamentally different as well. They allow us to store a collection of data with a single reference, and enable a much more convenient way to store and access collections of variables. Now what makes the array different from a Python list? The primary difference is that arrays in C/C++ are **immutable** in size. In that once you declare their size it **cannot** be changed. Take the following array as an example:

```c++

int arr[10];

```

It only has room to store 10 integer values, and while it can store less, it cannot store anymore than 10 elements. It should also be noted that with your current knowledge **variable length arrays are not valid**, so something like the following is invalid:

```c++

int len = 10;
int arr[len];

```

If you remember strings from last lab, C-style strings are actually just stored as arrays of character values terminated by a zero. The NULL terminator is an extremely useful part of a C-style string, however we cannot use a similar construct for arrays that hold number values.

:white_check_mark: Question 6. Why can we not NULL terminate an integer array?

There are two main ways to initialize an array in C++, with either an **initializer list** or with the use of a loop of some kind. The following code will show you syntax for both methods to initialize an array of 5 integer with the values from 1 - 5:

```c++

// Initialize List
int arr[5] = {1, 2, 3, 4, 5};

```

```c++

// With a for loop
int arr[5];

for(int i = 0 ; i < 5 ; i++) {
    arr[i] = i+1;
}

```

Moving on to some syntax the following program will initialize an array of integers and make a call to a function to print out the values in that array. That function is currently incomplete, there are in-line comments in each area that you need to complete:

```c++

void printArray(int arr[]);

// Initialize List
int arr[5] = {1, 2, 3, 4, 5};

printArray(arr);

void printArr(int arr[]){
    // Loop through all elements in the array
        // Print the value at each index
}

```

:white_check_mark: Question 7. Write a function *findMin* that accepts an array of ints and returns the smallest value in that array.

:white_check_mark: Question 8. Write a function *findMaxIndex* that accepts an array of ints and returns the index of the largest value in that array.

:white_check_mark: Question 9. Write a function *calculateMedian* that accepts an array of ints and returns the median.

:white_check_mark: Question 10. Write a function *replace* that accepts and array and two ints: *x*, and *n*. This function should replace all instances of *x* with *n*.

:white_check_mark: Question 11. Write a function *doubleEvens* that accepts an array and doubles all of the even values in that array.

:white_check_mark: Question 12. Write a function *multiModify* that accepts an array that triples all multiples of 3, doubles all multiples of 2, and ignores everything else. Note: A value should be able to be modified by multiple statements e.g. 6 would get tripled, then doubled.

:white_check_mark: Question 13. Write a function *split* that accepts three arrays, *original*, *evens*, and *odds*. The function should accept all 3 by reference, extract the evens & odds from *original*, and store them into *evens*, and *odds* respectively.
Note: You can use *sizeof(array) / sizeof(array[0])* to get the # of elements in an array. **This will only work within the scope that you declared the array in!** You'll need to figure out how to get the # of arrays within the function.


# Part 5. Submission [5 minutes]

Each group will submit a single **.zip file** named `lab-12.zip` containing all your answers to the lab questions in your `lab-07.txt` and all of your `.cpp` source code files on [Gradescope](http://gradescope.com) **before the end of your lab section**. **All submissions should be made by a group/team.** *Individual submissions will not be accepted.* Instructions to download your `lab-12.txt` file can be found in the IDE introduction page that you read in lab-01. For your convenience, that page is relinked [here](https://cs50.readthedocs.io/ide/online/).
