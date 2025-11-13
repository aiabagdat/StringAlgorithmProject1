# String Algorithm - KMP

This project implements the **Knuth-Morris-Pratt (KMP)** algorithm in Java to efficiently search for a pattern in a given text.

## Overview

The KMP algorithm is a string searching (or pattern matching) algorithm that improves the naive approach by using previously gathered information about the text and pattern to avoid redundant comparisons. It preprocesses the pattern to compute the **LPS (Longest Prefix Suffix)** array, which is then used during the search phase to skip unnecessary comparisons.

## Files

- `KMP.java`: Contains the implementation of the KMP algorithm.
- `test_case1.txt`: Test case for a short string.
- `test_case2.txt`: Test case for a medium-length string.
- `test_case3.txt`: Test case for a long string.
- `output.txt`: The output file where the results of the program are saved.
- `README.md`: This file containing project description and instructions.

## Time Complexity

- **Time Complexity**: **O(n + m)**, where:
  - `n` is the length of the text.
  - `m` is the length of the pattern.
- **Space Complexity**: **O(m)** for storing the LPS array, where `m` is the length of the pattern.

The time complexity is efficient as it reduces the problem from O(n * m) (in the naive approach) to O(n + m) by using previously computed information from the LPS array.

## Running the Program

1. **Compile the program**:

   In the terminal, navigate to the project directory and run the following command to compile the Java program:

   ```bash
   javac src/KMP.java
Run the program:
After compiling, run the program with the following command:

java -cp src KMP
This will execute the program and search for the specified pattern in the text. The output will be saved in the output.txt file.
View the output:
You can open the output.txt file to check the results of the program, which will show the index of the pattern found in the text.

Example output in output.txt:

Pattern found at index 10
Example Test Cases
Test case 1 (test_case1.txt): Short string
Text: "ABAB"
Pattern: "AB"
Expected output: Pattern found at index 0
Test case 2 (test_case2.txt): Medium-length string
Text: "ABABABABABABAB"
Pattern: "ABA"
Expected output: Pattern found at index 0, Pattern found at index 2, Pattern found at index 4, etc.
Test case 3 (test_case3.txt): Long string
A long string of 1000 characters.
Pattern: "AB"
The program will search for "AB" in the long string and output all indices where it appears.
Conclusion
The KMP algorithm significantly optimizes the process of finding a pattern in a string by preprocessing the pattern and utilizing this information to skip redundant character comparisons. This project demonstrates the implementation of KMP in Java and its efficiency compared to the naive approach.
