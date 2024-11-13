# Types-of-Arrays-CPlusPlus
Include iostream: This includes the input/output stream library, allowing the use of std::cout for console output.

Main Function

int main() {

The main function is the entry point of this C++ program.
1. Declaring an Array and Reading Uninitialized Elements

int scores[10]; // Junk data

    int scores[10];: Declares an array of 10 integers called scores. This array is not initialized, so it contains "junk" data (whatever values were in memory at those locations).

std::cout << "scores[0] : " << scores[0] << std::endl;
std::cout << "scores[1] : " << scores[1] << std::endl;

    Printing scores[0] and scores[1]: This outputs the uninitialized values at the first two positions of the scores array.

for (size_t i {0}; i < 10; ++i) {
    std::cout << "scores [" << i << "] : " << scores[i] << std::endl;
}

    Loop through all elements: The loop prints each element in scores from scores[0] to scores[9], showing the junk data currently held in the array.

2. Initializing Specific Elements of the Array

scores[0] = 20;
scores[1] = 21;
scores[2] = 22;

    Assigning values: Initializes the first three elements of scores.

for (size_t i {0}; i < 10; ++i) {
    std::cout << "scores [" << i << "] : " << scores[i] << std::endl;
}

    Printing updated array: This loop shows the initialized values in the first three elements and junk data in the remaining elements.

3. Assigning Values in a Loop

for (size_t i {0}; i < 10; ++i) {
    scores[i] = i * 10;
}

    Loop initialization: Assigns values to each element in scores as multiples of 10 (0, 10, 20, ..., 90).

for (size_t i {0}; i < 10; ++i) {
    std::cout << "scores [" << i << "] : " << scores[i] << std::endl;
}

    Print updated array: This loop displays the array after all elements have been initialized.

4. Declaring and Initializing an Array Simultaneously

double salaries[5] {12.7, 7.5, 13.2, 8.1, 9.3};

    double salaries[5] {...};: Declares a salaries array with five elements initialized with specific values.

for (size_t i {0}; i < 5; ++i) {
    std::cout << "salary[" << i << "] : " << salaries[i] << std::endl;
}

    Print array: This loop prints each element of the salaries array.

5. Partial Initialization of an Array

int families[5] {12, 7, 5};

    Partial Initialization: Initializes only the first three elements. The remaining two elements are automatically set to 0.

for (size_t i {0}; i < 5; ++i) {
    std::cout << "families[" << i << "] : " << families[i] << std::endl;
}

    Print partially initialized array: Displays the values in families, showing the initialized elements and the zero-filled elements.

6. Declaring an Array Without Specifying Size

int class_sizes[] {10, 12, 15, 11, 18, 17, 23, 56};

    int class_sizes[] {...};: Declares an array class_sizes and initializes it. The size is deduced from the number of elements (8 in this case).

for (auto value : class_sizes) {
    std::cout << "value : " << value << std::endl;
}

    Range-based for loop: Iterates over each element in class_sizes using auto to automatically deduce the element type, printing each value.

7. Declaring a Read-Only (Constant) Array

const int birds[] {10, 12, 15, 11, 18, 17, 23, 56};

    const int birds[] {...};: Declares an array birds as const, meaning its values cannot be modified.

for (size_t i {0}; i < 8; ++i) {
    std::cout << "birds : " << birds[i] << std::endl;
}

    Print constant array: This loop prints each element of the birds array. Attempting to modify birds would cause a compilation error.

8. Summing Elements of an Array

int scores2[] {2, 5, 8, 2, 5, 6, 9};
int sum {0};

    Declaring scores2 and sum: Defines an array scores2 and initializes it with specific values. sum is initialized to 0 and will store the sum of the array elements.

for (int element : scores2) {
    sum += element;
}

    Range-based for loop to calculate sum: Iterates over each element in scores2 and adds it to sum.

std::cout << "Score sum : " << sum << std::endl;

    Output the sum: Prints the total sum of elements in scores2.

Summary

This code shows various array operations in C++:

    Declaring arrays with or without initial values.
    Initializing specific elements and modifying arrays in loops.
    Using range-based loops for iteration.
    Handling partially initialized arrays and constant (read-only) arrays.
    Summing array elements and printing results.

These array operations are foundational for working with collections of data in C++.


