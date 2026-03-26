# FIRST STEPS GUIDE

Welcome to your journey in software development. This repository has been carefully designed to guide you through the fundamentals of programming — from setting up your work environment to building complete projects, including version control with Git.

---

> ⚠️ **Important Note**
>
> For effective learning: We strongly recommend completing all the initial activities (up through the final projects) **without the use of Artificial Intelligence tools**. The goal is for you to develop a deep understanding of core concepts and the ability to solve problems on your own. AI is a fantastic tool for later — not for skipping the learning process.

---

## TABLE OF CONTENTS

1. [Development Environment Setup](#development-environment-setup)
2. [Version Control with Git](#version-control-with-git)
3. [Programming Fundamentals](#programming-fundamentals)
4. [Exercises by Language](#exercises-by-language)
5. [Final Projects](#final-projects)
6. [Solutions](#solutions-to-the-first-exercises)
7. [Next Steps](#next-steps)

---

## DEVELOPMENT ENVIRONMENT SETUP

A good work environment is the foundation of a good programmer. Follow these steps to get everything ready.

### Essential Installations

#### Visual Studio Code (VS Code)
Source code editor. Lightweight, free, and highly extensible. Download it from [code.visualstudio.com](https://code.visualstudio.com).

#### Git
Version control system. Essential for managing your code and collaborating. Download it from [git-scm.com](https://git-scm.com). During installation, you can accept all default options.

#### Node.js *(Optional but recommended)*
Required for running modern development environments and some extensions like Live Server. Download it from [nodejs.org](https://nodejs.org) (LTS version).

### Recommended VS Code Extensions

Once VS Code is installed, open the extensions panel (`Ctrl+Shift+X`) and install the following:

| Extension | Purpose |
|---|---|
| Spanish Language Pack | Translates the VS Code interface into Spanish. |
| Prettier - Code formatter | Automatically formats your code on save, maintaining a consistent style. |
| Live Server | Launches a local server with live reloading for web development. |
| Better Comments | Colors and categorizes your comments (`TODO`, `!`, `?`, `*`). |
| Error Lens | Displays errors and warnings directly next to the line of code. |
| Postman | Allows you to test APIs directly from VS Code. |
| vscode-icons | Assigns visual icons to different file types. |

> **Recommended setup:** To have Prettier format on save, go to settings, search for **"format on save"** and enable it. Then set Prettier as the default formatter.

---

## VERSION CONTROL WITH GIT

Git lets you save "snapshots" of your project over time, experiment without fear, and collaborate with others. This is the basic workflow you'll use every day.

### Verify Installation

Open a terminal (in VS Code: `Terminal > New Terminal`) and run:

```bash
git --version
```

If you see a version number, you're good to go. If not, check your installation.

### Clone this Repository

To get a local copy of this project on your computer:

```bash
git clone https://github.com/ggrauggas/FIRST-STEPS-GUIDE
```

If you want to access each `[REPOSITORY-URL]`, the address can be found in the **"Code"** button on the repository's GitHub page.

### Branch Management

Branches are independent lines of development. The main branch is usually called `main` or `master`. For your exercises, you'll create your own branch.

**Create a new branch and switch to it:**

```bash
git checkout -b my-exercises-branch
```

**Switch between existing branches:**

```bash
git checkout branch-you-want-to-switch-to
```

### Daily Workflow: Add, Commit, and Push

**1. Check the status of your changes:**

```bash
git status
```

This command shows you which files have been modified or added.

**2. Add changes to the staging area:**

To add a specific file:

```bash
git add filename.py
```

To add all modified files:

```bash
git add .
```

**3. Commit the changes with a message:**

```bash
git commit -m "Clear and concise description of what you did"
```

> Example: `git commit -m "Adds solution for the Persona class exercise in Python"`

**4. Push the changes to the remote repository (GitHub):**

```bash
git push origin my-exercises-branch
```

> If this is the first time you're pushing this branch, Git may ask you to set the upstream branch with the command it suggests.

---

# PROGRAMMING FUNDAMENTALS

Before writing a single line of code in Python or Java, these are the universal concepts you must master. Think of them as the building blocks you'll use to construct any program.

---

## Data Types

The data a program handles can be of different types.

| Type | Description | Python Example | Java Example |
|---|---|---|---|
| **String** | Text, any sequence of characters. | `name = "Ana"` | `String name = "Ana";` |
| **Integer** | Numbers without decimals. | `age = 30` | `int age = 30;` |
| **Float** | Numbers with a decimal point. | `height = 1.75` | `double height = 1.75;` |
| **Boolean** | True or false value. | `is_adult = True` | `boolean isAdult = true;` |

---

## Control Structures

These direct the flow of execution in a program.

### `if/else` Conditional

Executes a block of code only if a condition is met.

```python
# Python
age = 18
if age >= 18:
    print("You are an adult")
else:
    print("You are a minor")
```

```java
// Java
int age = 18;
if (age >= 18) {
    System.out.println("You are an adult");
} else {
    System.out.println("You are a minor");
}
```

### `for` Loop

Repeats a block of code a set number of times.

```python
# Python - Prints numbers 0 through 4
for i in range(5):
    print(i)
```

```java
// Java - Prints numbers 0 through 4
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
```

### `while` Loop

Repeats a block of code while a condition is true.

```python
# Python
counter = 0
while counter < 5:
    print(counter)
    counter += 1
```

```java
// Java
int counter = 0;
while (counter < 5) {
    System.out.println(counter);
    counter++;
}
```

---

## Modularity: Functions and Methods

Functions allow you to group a block of code that performs a specific task, so it can be reused.

```python
# Python - Define and call a function
def greet(name):
    return f"Hello, {name}"

message = greet("Carlos")
print(message)  # Output: Hello, Carlos
```

```java
// Java - Define and call a method
public class Utilities {
    public static String greet(String name) {
        return "Hello, " + name;
    }

    public static void main(String[] args) {
        String message = greet("Carlos");
        System.out.println(message);  // Output: Hello, Carlos
    }
}
```

---

## Object-Oriented Programming (OOP)

OOP is a paradigm that organizes code into "objects" containing data (**attributes**) and behaviors (**methods**).

- **Class:** The mold or template. It defines what an object will look like.
- **Object:** A concrete instance created from a class.

```python
# Python - Class definition
class Dog:
    # Constructor: called when creating an object
    def __init__(self, name, breed):
        self.name = name
        self.breed = breed

    # Method (behavior)
    def bark(self):
        return f"{self.name} says: Woof!"

# Create objects (instances)
dog_1 = Dog("Rex", "Border Collie")
dog_2 = Dog("Buddy", "Beagle")

print(dog_1.bark())     # Output: Rex says: Woof!
print(dog_2.name)       # Output: Buddy
```

```java
// Java - Class definition
public class Dog {
    // Attributes (properties)
    private String name;
    private String breed;

    // Constructor
    public Dog(String name, String breed) {
        this.name = name;
        this.breed = breed;
    }

    // Method (behavior)
    public String bark() {
        return this.name + " says: Woof!";
    }

    // Getter to access the private attribute
    public String getName() {
        return this.name;
    }

    public static void main(String[] args) {
        Dog myDog = new Dog("Rex", "Border Collie");
        Dog anotherDog = new Dog("Buddy", "Beagle");

        System.out.println(myDog.bark());
        System.out.println(anotherDog.getName());
    }
}
```

---

## Arrays, Lists, and Matrices

Collections allow you to store multiple values in a single variable.

### Arrays (fixed-size)

In Java, arrays have a fixed size defined at creation. Python has no native equivalent — lists are used instead (see next section).

```python
# Python - No native fixed array; can simulate with the array module
import array
numbers = array.array('i', [10, 20, 30, 40, 50])
print(numbers[0])   # Output: 10
print(len(numbers)) # Output: 5
```

```java
// Java - Fixed-size array
int[] numbers = {10, 20, 30, 40, 50};
System.out.println(numbers[0]);        // Output: 10
System.out.println(numbers.length);    // Output: 5

// Declare first, fill later
String[] colors = new String[3];
colors[0] = "red";
colors[1] = "green";
colors[2] = "blue";
```

### Lists (dynamic size)

Lists can grow or shrink at runtime.

```python
# Python - List (the most commonly used structure)
fruits = ["apple", "banana", "orange"]

# Add elements
fruits.append("grape")           # To the end: ["apple", "banana", "orange", "grape"]
fruits.insert(1, "kiwi")         # At position: ["apple", "kiwi", "banana", "orange", "grape"]

# Remove elements
fruits.remove("banana")          # By value
fruits.pop()                     # Removes the last one
fruits.pop(0)                    # Removes by index

# Access and iterate
print(fruits[0])                 # First element
print(fruits[-1])                # Last element (Python shortcut)
print(fruits[1:3])               # Slice: elements at index 1 and 2

for fruit in fruits:
    print(fruit)
```

```java
// Java - ArrayList (dynamic size, equivalent to Python list)
import java.util.ArrayList;

ArrayList<String> fruits = new ArrayList<>();

// Add elements
fruits.add("apple");
fruits.add("banana");
fruits.add("orange");
fruits.add(1, "kiwi");           // Insert at specific position

// Remove elements
fruits.remove("banana");         // By value
fruits.remove(0);                // By index

// Access and iterate
System.out.println(fruits.get(0));       // First element
System.out.println(fruits.size());       // List size

for (String fruit : fruits) {
    System.out.println(fruit);
}
```

### Useful shortcuts and common list operations

```python
# Python - Useful shortcuts

numbers = [3, 1, 4, 1, 5, 9, 2, 6]

# Sort
numbers.sort()                        # In-place sort: [1, 1, 2, 3, 4, 5, 6, 9]
sorted_list = sorted(numbers)         # Returns a new sorted list
numbers.sort(reverse=True)            # Descending order

# Search
print(3 in numbers)                   # True/False → check if exists
print(numbers.index(4))               # Index of first 4
print(numbers.count(1))               # How many times 1 appears

# Quick stats
print(min(numbers))                   # Minimum value
print(max(numbers))                   # Maximum value
print(sum(numbers))                   # Total sum
print(len(numbers))                   # Number of elements

# List comprehension (create lists in one line)
squares = [x**2 for x in range(1, 6)]      # [1, 4, 9, 16, 25]
evens = [x for x in numbers if x % 2 == 0] # Only even numbers

# Copy a list (don't use list2 = list1 — that doesn't copy)
copy = numbers.copy()
copy = numbers[:]                     # Alternative with slice

# Combine lists
a = [1, 2, 3]
b = [4, 5, 6]
c = a + b                             # [1, 2, 3, 4, 5, 6]
a.extend(b)                           # Appends b to the end of a
```

```java
// Java - Useful shortcuts with ArrayList and Arrays

import java.util.ArrayList;
import java.util.Arrays;
import java.util.Collections;

ArrayList<Integer> numbers = new ArrayList<>(Arrays.asList(3, 1, 4, 1, 5, 9, 2, 6));

// Sort
Collections.sort(numbers);                        // Ascending order
Collections.sort(numbers, Collections.reverseOrder()); // Descending order

// Search
System.out.println(numbers.contains(3));          // true/false
System.out.println(numbers.indexOf(4));           // Index of first 4
System.out.println(Collections.frequency(numbers, 1)); // How many times 1 appears

// Stats
System.out.println(Collections.min(numbers));     // Minimum value
System.out.println(Collections.max(numbers));     // Maximum value

// Copy
ArrayList<Integer> copy = new ArrayList<>(numbers);

// Combine lists
ArrayList<Integer> a = new ArrayList<>(Arrays.asList(1, 2, 3));
ArrayList<Integer> b = new ArrayList<>(Arrays.asList(4, 5, 6));
a.addAll(b);  // Appends b to the end of a
```

### Matrices (lists of lists / 2D arrays)

A matrix is a table of rows and columns. It is implemented as a list of lists.

```python
# Python - 3x3 matrix
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

# Access an element: matrix[row][column]
print(matrix[0][0])   # Output: 1  → row 0, column 0
print(matrix[1][2])   # Output: 6  → row 1, column 2

# Iterate through the entire matrix
for row in matrix:
    for element in row:
        print(element, end=" ")
    print()  # New line after each row

# Create an empty 3x3 matrix filled with zeros
rows, cols = 3, 3
empty = [[0] * cols for _ in range(rows)]
```

```java
// Java - 3x3 matrix (2D array)
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

// Access an element: matrix[row][column]
System.out.println(matrix[0][0]);   // Output: 1
System.out.println(matrix[1][2]);   // Output: 6

// Iterate through the entire matrix
for (int i = 0; i < matrix.length; i++) {
    for (int j = 0; j < matrix[i].length; j++) {
        System.out.print(matrix[i][j] + " ");
    }
    System.out.println();  // New line after each row
}

// Create an empty 3x3 matrix filled with zeros
int[][] empty = new int[3][3];  // Java initializes to 0 automatically
```

### Quick comparison: when to use each structure?

| Structure | Python | Java | When to use it |
|---|---|---|---|
| **Fixed array** | `array.array` | `int[]` | Known size, maximum performance |
| **Dynamic list** | `list` | `ArrayList` | Variable size, general use |
| **2D matrix** | `list` of `list` | `int[][]` | Tables, grids, images |

---

## EXERCISES BY LANGUAGE

Below are the exercises you need to complete for each technology. It is recommended to do them in order.

### 🐍 PYTHON

Python is ideal for beginners due to its clear and readable syntax. Run files with:

```bash
python filename.py
```

| # | Exercise | Description | Key Concepts |
|---|---|---|---|
| 1 | **Hello World** | Print the text `"Hello, world!"` to the console. | `print()` |
| 2 | **Math Operations** | Declare two numeric variables and display the result of their sum, subtraction, multiplication, and division. | Variables, data types, arithmetic operators. |
| 3 | **User Input and Conditional** | Ask the user for their age using `input()` and display whether they are an adult (>= 18) or not. | `input()`, type conversion (`int()`), `if/else` conditional. |
| 4 | **Loop Validation** | Ask the user to enter the number 5. If they enter something else, keep asking. At the end, display `"Correct!"`. | `while` loop, conditionals. |
| 5 | **Object-Oriented Programming** | Create a `Person` class with attributes `name`, `age`, `weight`, and `height`. Include a `show_info()` method. Create two objects and display their information. | Classes, `__init__` constructor, methods, `self`. |

### ☕ JAVA

Java is a strongly typed, compiled language. You'll need to install the **JDK** (Java Development Kit). To compile and run:

```bash
javac FileName.java   # Compile
java FileName         # Run
```

| # | Exercise | Description | Key Concepts |
|---|---|---|---|
| 1 | **Hello World** | Create a class with a `main` method that prints `"Hello, world!"`. | Class structure, `main` method, `System.out.println()`. |
| 2 | **Scanner and Input** | Use the `Scanner` class to ask the user for their name and age, then print them. | `java.util.Scanner`, `nextLine()`, `nextInt()`. |
| 3 | **Conditional Logic** | Ask the user for their age and determine whether they are an adult with `if-else`. | `if-else`, comparison operators. |
| 4 | **Object-Oriented Programming** | Create a `Person` class with private attributes, a constructor, getters, and setters. In `main`, create a person and display their data. | `private`, `public`, encapsulation, getters/setters. |

### 🌐 HTML AND CSS

These technologies define the structure and style of web pages. No compilation needed — just open the `.html` file in a browser.

| # | Exercise | Description | Key Concepts |
|---|---|---|---|
| 1 | **Basic Structure** | Create an HTML document with an `h1` heading, a `p` paragraph, and a `div` with text. | `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`, `h1`, `p`, `div`. |
| 2 | **Form** | Add a form with fields for name and age, and a submit button. | `<form>`, `<input type="text">`, `<input type="number">`, `<button>`. |
| 3 | **CSS Styles** | Apply styles: first inline (`style`), then with `<style>` in `<head>`, and finally with an external `styles.css` file. | `color`, `background-color`, `margin`, `padding`, CSS selectors. |

### 🟨 JAVASCRIPT

JavaScript adds interactivity to web pages. It runs in the browser.

| # | Exercise | Description | Key Concepts |
|---|---|---|---|
| 1 | **Basic Interactivity** | Create a button that, when clicked, shows an alert with `"Button clicked!"`. | `onclick` event, `alert()` function. |
| 2 | **Capture and Display Data** | Write a function that captures the form values (name and age) and displays them in a paragraph, without using `alert()`. | `document.getElementById()`, `.value`, DOM manipulation (`.innerText`). |

---

## FINAL PROJECTS

These projects integrate all the knowledge you've acquired. Complete them after finishing the individual exercises.

### Web Calculator [HTML, CSS, JAVASCRIPT]

Build a functional calculator that can perform the four basic operations: addition, subtraction, multiplication, and division.

**Expected structure:**

- **HTML:** An interface with two `<input type="number">` fields, four buttons (`+`, `-`, `*`, `/`), and an area to display the result.
- **CSS:** Styles to make it visually appealing: large buttons, differentiated colors, centered on screen.
- **JavaScript:** Logic to capture values, perform the operation, handle division by zero, and display the result.

**Base code example (sum function):**

```javascript
function add() {
    // Get values from inputs and convert them to numbers
    let number1 = parseFloat(document.getElementById('num1').value);
    let number2 = parseFloat(document.getElementById('num2').value);
    
    // Perform the addition
    let result = number1 + number2;
    
    // Display the result in the element with id="result"
    document.getElementById('result').innerText = "Result: " + result;
}
```

### ❌⭕ TIC-TAC-TOE IN THE CONSOLE [PYTHON OR JAVA]

Implement the classic Tic-Tac-Toe game in text mode through the console. You can choose **Python** or **Java**.

**Game logic:**

1. **Represent the board:** Use a 3×3 list (Python) or array (Java). Empty positions are represented with `" "`.

2. **Display the board** in a readable way:

    ```
       |   | 
    ---+---+---
       |   |  
    ---+---+---
       |   | 
    ```
    
    ```
     X | O | X
    ---+---+---
       | O |  
    ---+---+---
     O | X | X
    ```

3. **Turns:** Alternate between player `"X"` and player `"O"`.

4. **User input:** Ask for the move coordinates (row and column, from 0 to 2).

5. **Validations:**
   - The chosen cell must be empty.
   - Coordinates must be within the valid range.

6. **Winner check:** After each move, check if there are three in a row (horizontal, vertical, or diagonal). If there's a winner, announce it and end the game.

7. **Draw:** If the board fills up with no winner, announce a draw and end the game.

---

## SOLUTIONS TO THE FIRST EXERCISES

> 💡 Try to solve the exercises on your own before checking the solutions.

### Python Solutions

#### Exercise 1: Hello World

```python
# hello_world.py
print("Hello, world!")
```

#### Exercise 2: Math Operations

```python
# operations.py
number1 = 10
number2 = 5

sum_result = number1 + number2
subtraction = number1 - number2
multiplication = number1 * number2
division = number1 / number2

print("Sum:", sum_result)
print("Subtraction:", subtraction)
print("Multiplication:", multiplication)
print("Division:", division)
```

#### Exercise 3: User Input and Conditional

```python
# age.py
age_str = input("Please enter your age: ")
age = int(age_str)

if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

#### Exercise 4: Loop Validation

```python
# number_validation.py
correct_number = 5
user_number = None

while user_number != correct_number:
    user_number_str = input("Enter the number 5: ")
    user_number = int(user_number_str)
    
    if user_number != correct_number:
        print("Incorrect. Try again.")

print("Correct!")
```

#### Exercise 5: Object-Oriented Programming (Person Class)

```python
# person.py
class Person:
    def __init__(self, name, age, weight, height):
        self.name = name
        self.age = age
        self.weight = weight    # in kilograms
        self.height = height    # in meters
    
    def show_info(self):
        print("--- Person Information ---")
        print(f"Name: {self.name}")
        print(f"Age: {self.age} years")
        print(f"Weight: {self.weight} kg")
        print(f"Height: {self.height} m")
        print("--------------------------")

# Create objects and display their information
person1 = Person("Ana Garcia", 28, 60.5, 1.65)
person2 = Person("Luis Perez", 35, 82.0, 1.78)

person1.show_info()
person2.show_info()
```

### Java Solutions

#### Exercise 1: Hello World

```java
// HelloWorld.java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

#### Exercise 2: Scanner and Input

```java
// UserInput.java
import java.util.Scanner;

public class UserInput {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter your name: ");
        String name = scanner.nextLine();
        
        System.out.print("Enter your age: ");
        int age = scanner.nextInt();
        
        System.out.println("Hello " + name + ", you are " + age + " years old.");
        
        scanner.close();
    }
}
```

#### Exercise 3: Conditional Logic (Adult Check)

```java
// AdultCheck.java
import java.util.Scanner;

public class AdultCheck {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter your age: ");
        int age = scanner.nextInt();
        
        if (age >= 18) {
            System.out.println("You are an adult.");
        } else {
            System.out.println("You are a minor.");
        }
        
        scanner.close();
    }
}
```

#### Exercise 4: Object-Oriented Programming (Person Class with Getter/Setter)

```java
// Person.java
public class Person {
    // Private attributes (encapsulation)
    private String name;
    private int age;
    
    // Constructor
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    
    // Getter for name
    public String getName() {
        return this.name;
    }
    
    // Setter for name
    public void setName(String name) {
        this.name = name;
    }
    
    // Getter for age
    public int getAge() {
        return this.age;
    }
    
    // Setter for age
    public void setAge(int age) {
        if (age >= 0) {
            this.age = age;
        } else {
            System.out.println("Invalid age");
        }
    }
    
    public void showInfo() {
        System.out.println("Name: " + this.name);
        System.out.println("Age: " + this.age);
    }
    
    public static void main(String[] args) {
        Person person = new Person("Carlos", 25);
        
        System.out.println("--- Initial Data ---");
        person.showInfo();
        
        // Use setters to modify
        person.setName("Carlos Lopez");
        person.setAge(26);
        
        System.out.println("\n--- Updated Data ---");
        person.showInfo();
    }
}
```

### HTML, CSS, and JavaScript Solutions

#### Exercises 1 and 2: Structure, Form, and Interactivity

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Interactive Page</title>
    
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        h1 { color: #333; text-align: center; }
        .form-container {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            margin-bottom: 20px;
        }
        .field { margin-bottom: 15px; }
        label { display: block; margin-bottom: 5px; font-weight: bold; }
        input[type="text"], input[type="number"] {
            width: 100%;
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
        }
        button {
            background-color: #007bff;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin-right: 10px;
        }
        button:hover { background-color: #0056b3; }
        .result {
            background-color: #e9ecef;
            padding: 15px;
            border-radius: 4px;
            margin-top: 15px;
        }
    </style>
</head>
<body>
    <h1>User Form</h1>
    
    <div class="form-container">
        <div class="field">
            <label for="name">Name:</label>
            <input type="text" id="name" placeholder="Enter your name">
        </div>
        <div class="field">
            <label for="age">Age:</label>
            <input type="number" id="age" placeholder="Enter your age">
        </div>
        <button onclick="showData()">Show Data</button>
        <button onclick="showAlert()">Show Alert</button>
        <div class="result" id="result">Data will be shown here...</div>
    </div>
    
    <div class="form-container">
        <h3>Simple Calculator</h3>
        <div class="field">
            <label for="num1">Number 1:</label>
            <input type="number" id="num1">
        </div>
        <div class="field">
            <label for="num2">Number 2:</label>
            <input type="number" id="num2">
        </div>
        <button onclick="operate('add')">+</button>
        <button onclick="operate('subtract')">-</button>
        <button onclick="operate('multiply')">*</button>
        <button onclick="operate('divide')">/</button>
        <div class="result" id="calculatorResult">Result: </div>
    </div>
    
    <script>
        function showData() {
            let name = document.getElementById('name').value;
            let age = document.getElementById('age').value;
            let resultDiv = document.getElementById('result');
            
            if (name && age) {
                resultDiv.innerHTML = `
                    <strong>Entered data:</strong><br>
                    Name: ${name}<br>
                    Age: ${age} years old<br>
                    ${age >= 18 ? 'Is an adult' : 'Is a minor'}
                `;
            } else {
                resultDiv.innerHTML = 'Please fill in all fields.';
            }
        }
        
        function showAlert() {
            alert('Button clicked! This is the alert message.');
        }
        
        function operate(type) {
            let num1 = parseFloat(document.getElementById('num1').value);
            let num2 = parseFloat(document.getElementById('num2').value);
            let result, operator;
            
            if (isNaN(num1) || isNaN(num2)) {
                document.getElementById('calculatorResult').innerHTML =
                    'Result: Please enter both numbers.';
                return;
            }
            
            switch(type) {
                case 'add':      result = num1 + num2; operator = '+'; break;
                case 'subtract': result = num1 - num2; operator = '-'; break;
                case 'multiply': result = num1 * num2; operator = '*'; break;
                case 'divide':
                    if (num2 === 0) {
                        document.getElementById('calculatorResult').innerHTML =
                            'Result: Error, cannot divide by zero.';
                        return;
                    }
                    result = num1 / num2; operator = '/'; break;
                default: return;
            }
            
            document.getElementById('calculatorResult').innerHTML =
                `Result: ${num1} ${operator} ${num2} = ${result}`;
        }
    </script>
</body>
</html>
```

**Code explanation:**

- **HTML structure:** Two main containers: a user form and a simple calculator.
- **CSS styles:** Font, colors, spacing, rounded borders, and shadows. The `.form-container` class selector is used to reuse styles.
- **JavaScript:**
  - `showData()` — Gets values with `getElementById()`, validates them, and modifies the DOM with `.innerHTML`.
  - `showAlert()` — Example of interaction with `alert()`.
  - `operate(type)` — Calculator logic with validations (empty fields, division by zero).

---

## NEXT STEPS

Once you've completed all the exercises and final projects, you'll be ready to explore more advanced topics:

- **File handling** — reading and writing to disk.
- **Database connections.**
- **Web frameworks** — Flask/Django (Python), Spring Boot (Java), React (JavaScript).
- **Unit testing.**
- **Application deployment.**

---

*Congratulations on taking your first step in your career as a developer!*
