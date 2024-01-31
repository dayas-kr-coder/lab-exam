Programming in C++

- (Q) Input the three coefficients of a quadratic equation and find the roots.

```cpp

```

- (Q) Input a digit and display the same in word. (Zero for 0, One for 1, ...., Nine for 9)

```cpp
#include <iostream>
using namespace std;

int main()
{
  int num;
  cout << "Enter a digit between (0 - 9): ";
  cin >> num;

  switch(num) {
    case 0 : cout << "Zero" << endl;
    break;
    case 1 : cout << "One" << endl;
    break;
    case 2 : cout << "Two" << endl;
    break;
    case 3 : cout << "Three" << endl;
    break;
    case 4 : cout << "Four" << endl;
    break;
    case 5 : cout << "Five" << endl;
    break;
    case 6 : cout << "Six" << endl;
    break;
    case 7 : cout << "Seven" << endl;
    break;
    case 8 : cout << "Eight" << endl;
    break;
    case 9 : cout << "Nine" << endl;
    break;
    default : cout << "Invailed Entry!" << endl;
    break;
  }

  return 0;
}
```

- (Q) Find the sum of the squares of the first N natural numbers without using formula.

```cpp
#include <iostream>
using namespace std;

int main()
{
  int num, i, sum = 0;
  cout << "Enter a number: ";
  cin >> num;

  for(i = 0; i<=num; i++) {
    sum += + i * i;
  }

  cout << "Sum of square of first " << num << " natural numbers : " << sum << endl;

  return 0;
}
```

- (Q) Input an integer number and check whether it is palindrome or not.

```cpp
#include <iostream>
using namespace std;

int main()
{
  int num, rem, copy, rev = 0;
  cout << "Enter a number : ";
  cin >> num;
  copy = num;

  while(num > 0) {
    rem = num % 10;
    rev = rev * 10 + rem;
    num = num / 10;
  }

  if(rev == copy)
    cout << "The given number is Palindrome." << endl;
  else
    cout << "The given number is not Palindrome." << endl;

  return 0;
}
```

- (Q) Input an integer number and check whether it is a prime or not.

```cpp

```

- (Q) Create an array to store the heights of some students and sort the values.

```cpp
#include <iostream>
#include <algorithm> // for std::sort
using namespace std;

int main() {
    const int maxSize = 10; // Maximum size of the array
    float heights[maxSize];

    int numStudents;

    // Input the number of students
    cout << "Enter the number of students: ";
    cin >> numStudents;

    // Input heights of students
    cout << "Enter the heights of students:\n";
    for (int i = 0; i < numStudents; i++) {
        cout << "Student " << i + 1 << ": ";
        cin >> heights[i];
    }

    // Use std::sort to sort the heights in ascending order
    sort(heights, heights + numStudents);

    // Display the sorted heights
    cout << "\nSorted Heights:\n";
    for (int i = 0; i < numStudents; i++) {
        cout << "Student " << i + 1 << ": " << heights[i] << " cm\n";
    }

    return 0;
}

```

- (Q) Find the length of a string without using strlen() function.

```cpp
#include <iostream>
using namespace std;

int main() {
    // Input a string
    cout << "Enter a string: ";
    char str[100];
    cin.getline(str, 100);

    // Calculate the length of the string without using strlen()
    int length = 0;
    while (str[length] != '\0') {
        length++;
    }

    // Display the length of the string
    cout << "Length of the string: " << length << endl;

    return 0;
}

```

- (Q) Define a function to find the factorial of a number. Using this function find the value of nCr.

```cpp

```

- (Q) Create a structure to represent admission number, name and marks given for CE, PE and TE of a subject. Input the details of a student and display admission number, name and total marks obtained.

```cpp
#include <iostream>
using namespace std;

// Structure to represent student details
struct Student {
    int admissionNumber;
    string name;
    float ceMarks; // Classroom Exam Marks
    float peMarks; // Practical Exam Marks
    float teMarks; // Theory Exam Marks
};

// Function to calculate total marks
float calculateTotalMarks(const Student& student) {
    return student.ceMarks + student.peMarks + student.teMarks;
}

int main() {
    // Declare a Student structure variable
    Student student;

    // Input details of the student
    cout << "Enter Admission Number: ";
    cin >> student.admissionNumber;

    cin.ignore(); // Ignore the newline character in the input buffer

    cout << "Enter Name: ";
    getline(cin, student.name);

    cout << "Enter Classroom Exam Marks: ";
    cin >> student.ceMarks;

    cout << "Enter Practical Exam Marks: ";
    cin >> student.peMarks;

    cout << "Enter Theory Exam Marks: ";
    cin >> student.teMarks;

    // Calculate total marks
    float totalMarks = calculateTotalMarks(student);

    // Display details and total marks
    cout << "\nStudent Details:\n";
    cout << "Admission Number: " << student.admissionNumber << endl;
    cout << "Name: " << student.name << endl;
    cout << "Total Marks Obtained: " << totalMarks << endl;

    return 0;
}
```

- (Q) 10.Input numbers and swap them by defining a function with pointer arguments.

```cpp
#include <iostream>
using namespace std;

// Function to swap two numbers using pointers
void swapNumbers(int* num1, int* num2) {
    int temp = *num1;
    *num1 = *num2;
    *num2 = temp;
}

int main() {
    int num1, num2;

    // Input two numbers
    cout << "Enter the first number: ";
    cin >> num1;
    cout << "Enter the second number: ";
    cin >> num2;

    // Display the original numbers
    cout << "Original numbers: " << num1 << " and " << num2 << endl;

    // Call the swap function with pointers
    swapNumbers(&num1, &num2);

    // Display the swapped numbers
    cout << "Swapped numbers: " << num1 << " and " << num2 << endl;

    return 0;
}
```
