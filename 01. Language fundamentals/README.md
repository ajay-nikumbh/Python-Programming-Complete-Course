<p align="center">
  <img src="https://www.python.org/static/community_logos/python-logo-generic.svg" alt="Python logo" width="320">
</p>

# 01. Language Fundamentals

This topic answers the first questions every learner has: what Python is, where it came from, why so many people use it, where it is used, and what its strengths and limits are. There is very little code here. The goal is to build a clear picture of the language before you start writing programs.

**In this topic**

1. [What is Python?](#1-what-is-python)
2. [History of Python](#2-history-of-python)
3. [Why the name "Python"?](#3-why-the-name-python)
4. [Python compared with Java and C](#4-python-compared-with-java-and-c)
5. [Where Python's features came from](#5-where-pythons-features-came-from)
6. [Where we can use Python](#6-where-we-can-use-python)
7. [Features of Python](#7-features-of-python)
8. [Limitations of Python](#8-limitations-of-python)
9. [Flavors of Python](#9-flavors-of-python)
10. [Python versions](#10-python-versions)
11. [Quick revision](#11-quick-revision)
12. [Practice questions](#12-practice-questions)

---

## 1. What is Python?

> **Python is a general purpose, high level programming language.**

These two words are worth understanding properly:

| Term | Simple meaning | Example |
|------|----------------|---------|
| **General purpose** | Not built for one job only. You can use it to make many kinds of software. | Websites, games, data analysis, automation scripts, machine learning |
| **High level** | Close to human language, far from machine language. The language handles hardware details for you. | You write `print("Hi")`. You do not manage memory or CPU registers. |

The levels of programming languages, from the machine up to the programmer:

```mermaid
flowchart BT
    M["Machine language<br/>0s and 1s, the CPU understands this directly"]
    A["Assembly language<br/>Short codes like MOV, ADD"]
    H["High level languages<br/>Python, Java, C++<br/>Close to English, easy for humans"]
    M --> A --> H
```

Python is often recommended as the **first programming language for beginners** because its programs are short and easy to read.

---

## 2. History of Python

- Python was developed by **Guido van Rossum** in **1989**.
- He was working at the **National Research Institute for Mathematics and Computer Science (CWI)** in the **Netherlands**.
- Python was officially released to the public in **1991**.
- The official date of birth of Python is **20 February 1991**.

```mermaid
flowchart LR
    A["1989<br/>Guido van Rossum starts<br/>building Python at CWI"] --> B["20 Feb 1991<br/>First public release"]
    B --> C["Jan 1994<br/>Python 1.0"]
    C --> D["Oct 2000<br/>Python 2.0"]
    D --> E["Dec 2008<br/>Python 3.0"]
    E --> F["Jan 2020<br/>Python 2 reaches<br/>end of life"]
    F --> G["Today<br/>Python 3.x"]
```

---

## 3. Why the name "Python"?

The name has nothing to do with the snake. Guido van Rossum took the name from the BBC comedy TV show **"Monty Python's Flying Circus"**, which was broadcast from **1969 to 1974**. He wanted a name that was short, unique and a little mysterious.

---

## 4. Python compared with Java and C

The best way to see why Python is called simple is to write the same program in three languages.

### Example 1: Print "Hello World"

<table width="100%">
<tr>
<th width="33%"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" alt="Java logo" height="28"><br/>Java</th>
<th width="33%"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" alt="C logo" height="28"><br/>C</th>
<th width="34%"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="Python logo" height="28"><br/>Python</th>
</tr>
<tr>
<td valign="top">

```java
public class HelloWorld
{
    public static void main(String[] args)
    {
        System.out.println("Hello world");
    }
}
```

</td>
<td valign="top">

```c
#include <stdio.h>

void main()
{
    printf("Hello world");
}
```

</td>
<td valign="top">

```python
print("Hello World")
```

</td>
</tr>
<tr>
<td align="center">7 lines</td>
<td align="center">6 lines</td>
<td align="center"><b>1 line</b></td>
</tr>
</table>

In Python, the same program needs no class, no `main` function, no header file and no semicolons.

```python
# Print a message on the screen
print("Hello World")
```

**Output**

```text
Hello World
```

### Example 2: Print the sum of two numbers

<table width="100%">
<tr>
<th width="33%"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" alt="Java logo" height="28"><br/>Java</th>
<th width="33%"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" alt="C logo" height="28"><br/>C</th>
<th width="34%"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="Python logo" height="28"><br/>Python</th>
</tr>
<tr>
<td valign="top">

```java
public class Add
{
    public static void main(String[] args)
    {
        int a, b;
        a = 10;
        b = 20;
        System.out.println("The Sum:" + (a + b));
    }
}
```

</td>
<td valign="top">

```c
#include <stdio.h>

void main()
{
    int a, b;
    a = 10;
    b = 20;
    printf("The Sum:%d", (a + b));
}
```

</td>
<td valign="top">

```python
a = 10
b = 20
print("The Sum:", (a + b))
```

</td>
</tr>
</table>

The Python version with comments:

```python
# Store the first number in the variable a
a = 10

# Store the second number in the variable b
b = 20

# Add a and b, then print the label and the result
print("The Sum:", (a + b))
```

**Output**

```text
The Sum: 30
```

**How this program runs**

```mermaid
flowchart TD
    S([Start]) --> A["a = 10<br/>Python creates the value 10 and names it a"]
    A --> B["b = 20<br/>Python creates the value 20 and names it b"]
    B --> C["a + b<br/>Python adds the values: 10 + 20 = 30"]
    C --> D["print(...)<br/>Shows: The Sum: 30"]
    D --> E([End])
```

1. Line 1 stores `10` in `a`.
2. Line 2 stores `20` in `b`.
3. Line 3 first works out `a + b`, which is `30`. Then `print()` shows the text `The Sum:` and the number `30`. `print()` puts a space between the two items automatically.

**What to notice:** In Java and C we must say that `a` and `b` are `int` before we use them. In Python we just assign the value. Python works out the type by itself. This is called **dynamic typing** (see [feature 6](#feature-6-dynamically-typed)).

---

## 5. Where Python's features came from

Guido van Rossum did not invent everything from zero. He took the best ideas from languages that already existed and combined them.

```mermaid
flowchart LR
    C["C"] -->|"Procedural / functional style<br/>(functions that do one task)"| P(("Python"))
    CPP["C++"] -->|"Object oriented programming<br/>(classes and objects)"| P
    PERL["Perl and Shell Script"] -->|"Scripting features<br/>(short programs that automate tasks)"| P
    MOD["Modula-3"] -->|"Modular programming<br/>(split code into modules)"| P
    ABC["C and ABC"] -->|"Most of the syntax"| P
```

| Feature | Taken from | What it means for you |
|---------|-----------|------------------------|
| Functional programming features | C | Write a program as a set of functions, each doing one job |
| Object oriented programming features | C++ | Model real things as classes and objects (Topics 26 to 29) |
| Scripting language features | Perl and Shell Script | Write short programs that automate everyday tasks |
| Modular programming features | Modula-3 | Split a big program into small files called modules (Topic 11) |
| Most of the syntax | C and ABC | ABC was a teaching language Guido worked on before Python. Its clean, indentation based style shaped Python. |

> **Note:** C is usually called a *procedural* language. The notes call these "functional programming features" because in C you build a program out of functions. Python also has true functional programming tools such as `lambda`, `map()` and `filter()`, which came from languages like Lisp and Haskell. You will learn them in Topics 10 and 10.1.

---

## 6. Where we can use Python

We can use Python almost everywhere. The most common application areas are:

```mermaid
flowchart TD
    P(("Python")) --> D["Desktop applications"]
    P --> W["Web applications"]
    P --> DB["Database applications"]
    P --> N["Network programming"]
    P --> G["Game development"]
    P --> DA["Data analysis"]
    P --> ML["Machine learning"]
    P --> AI["Artificial intelligence"]
    P --> IOT["Internet of Things (IoT)"]
```

| Area | What you build | Popular tools |
|------|---------------|---------------|
| Desktop applications | Programs with windows and buttons | Tkinter, PyQt |
| Web applications | Websites and web APIs | Django, Flask, FastAPI |
| Database applications | Programs that store and read data | sqlite3, MySQL and PostgreSQL drivers (Topic 23) |
| Network programming | Programs that talk over a network | socket, requests |
| Games | 2D games | Pygame |
| Data analysis | Reports, charts and statistics from data | pandas, NumPy, Matplotlib |
| Machine learning | Programs that learn from data | scikit-learn, TensorFlow, PyTorch |
| Artificial intelligence | Language, vision and decision systems | PyTorch, Hugging Face libraries |
| IoT | Code for small devices and sensors | MicroPython on Raspberry Pi and microcontrollers |

**Who uses Python?**

- Google and YouTube use Python internally.
- NASA and the New York Stock Exchange have built applications with Python.
- Large software companies such as Google, Microsoft, IBM and Yahoo use Python.

---

## 7. Features of Python

Python is popular because of these 11 features.

```mermaid
flowchart LR
    P(("Features of<br/>Python")) --> F1["1. Simple and easy to learn"]
    P --> F2["2. Freeware and open source"]
    P --> F3["3. High level"]
    P --> F4["4. Platform independent"]
    P --> F5["5. Portable"]
    P --> F6["6. Dynamically typed"]
    P --> F7["7. Procedure and object oriented"]
    P --> F8["8. Interpreted"]
    P --> F9["9. Extensible"]
    P --> F10["10. Embedded"]
    P --> F11["11. Extensive library"]
```

### Feature 1: Simple and easy to learn

- A Python program reads almost like English sentences.
- The syntax is very simple, and there are only about **35 keywords** (reserved words). Java has about 50.
- We can write programs with far fewer lines than in other languages. This gives more **readability** and **simplicity**.
- Fewer lines mean less development time and lower project cost.

Look how close this program is to plain English:

```python
# Create a list of three student names
students = ["Asha", "Ravi", "Meena"]

# Go through the list one name at a time
for name in students:

    # Print a welcome message for the current name
    print("Welcome,", name)
```

**Output**

```text
Welcome, Asha
Welcome, Ravi
Welcome, Meena
```

**How this program runs:** Python takes the first name, `"Asha"`, puts it in `name` and runs the `print()` line. Then it does the same for `"Ravi"` and then for `"Meena"`. When the list has no more names, the loop stops. You can read the code aloud as: *"for each name in students, print welcome and the name."*

You can ask Python itself how many keywords it has:

```python
# Load the built-in keyword module
import keyword

# Count the keywords and print the count
print(len(keyword.kwlist))

# Print the full list of keywords
print(keyword.kwlist)
```

**Output** (Python 3.12)

```text
35
['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```

> The notes say "30+ keywords". The exact number changes a little between versions. Python 3.12 has 35. You will study keywords in detail in Topic 02.

### Feature 2: Freeware and open source

- **Freeware:** Python is free. You do not need to buy a licence to use it, even for commercial work.
- **Open source:** The source code of Python is open to everyone. Anyone can read it and change it for their needs.

**Example:** Jython is a customised version of Python made to work with Java applications. It was possible to build only because Python is open source.

### Feature 3: High level programming language

Python is a high level language, so it is **programmer friendly**. As a programmer you do not need to manage low level work such as:

- memory management (asking for memory and giving it back)
- security details of the hardware
- CPU registers and memory addresses

Python does this for you, so you can focus on solving the problem.

<table width="100%">
<tr>
<th width="50%">In C you manage memory yourself</th>
<th width="50%">In Python memory is automatic</th>
</tr>
<tr>
<td valign="top">

```c
int *marks = malloc(3 * sizeof(int));
marks[0] = 78;
marks[1] = 85;
marks[2] = 92;
free(marks);
```

</td>
<td valign="top">

```python
marks = [78, 85, 92]
```

</td>
</tr>
</table>

In C, if you forget `free()`, the program wastes memory. In Python you just create the list. Python frees the memory when the list is no longer used.

### Feature 4: Platform independent

You write a Python program **once**, and it runs on **any platform** (Windows, macOS, Linux) without rewriting it. Internally, the **PVM (Python Virtual Machine)** converts the program into a form that the machine understands.

```mermaid
flowchart TD
    S["hello.py<br/>Written once"] --> W["PVM on Windows"]
    S --> M["PVM on macOS"]
    S --> L["PVM on Linux"]
    W --> WO["Same output"]
    M --> MO["Same output"]
    L --> LO["Same output"]
```

The same `.py` file works everywhere because each operating system has its own PVM. The PVM hides the differences between the systems.

### Feature 5: Portability

Python programs are **portable**. You can move (migrate) a program from one platform to another very easily, and it gives the **same results** on every platform.

> **Platform independent vs portable:** Platform independent means the same code *can* run on any platform. Portable means *moving* the program to another platform is easy and the results stay the same. The two ideas are closely linked.

### Feature 6: Dynamically typed

In Python you do **not** declare the type of a variable. When you assign a value, Python looks at the value and gives the variable the right type automatically. That is why Python is called a **dynamically typed** language.

Java and C are **statically typed** languages, because you must give the type at the beginning.

<table width="100%">
<tr>
<th width="50%">Statically typed (Java)</th>
<th width="50%">Dynamically typed (Python)</th>
</tr>
<tr>
<td valign="top">

```java
int value = 10;
value = "ten";   // Error: a String is not an int
```

</td>
<td valign="top">

```python
value = 10
value = "ten"    # Allowed
```

</td>
</tr>
</table>

```python
# Assign a whole number, so Python makes value an int
value = 10

# Print the value and its type
print(value, type(value))

# Assign text to the same name, so value is now a str
value = "ten"

# Print the new value and its new type
print(value, type(value))
```

**Output**

```text
10 <class 'int'>
ten <class 'str'>
```

**How this program runs:** On line 1, Python sees `10`, which is a whole number, so `value` refers to an `int`. On line 3, we give the same name a piece of text, so now `value` refers to a `str`. We never wrote `int` or `str` ourselves. This flexibility makes coding faster. The cost is that a type mistake shows up only when the program runs, so read your code carefully.

### Feature 7: Both procedure oriented and object oriented

Python supports both styles:

- **Procedure oriented**, like C and Pascal: the program is a set of steps and functions.
- **Object oriented**, like C++ and Java: the program is built from classes and objects.

So we get the benefits of both, for example **security** and **reusability**. Beginners can start with simple procedural code and move to object oriented code later (Topics 26 to 29).

### Feature 8: Interpreted

You do not need to compile a Python program explicitly. The Python interpreter takes care of compilation internally.

- If the compilation fails, the interpreter raises a **syntax error**.
- If the compilation succeeds, the **PVM (Python Virtual Machine)** executes the program.

```mermaid
flowchart LR
    A["Source code<br/>hello.py"] --> B{"Compile<br/>(done automatically)"}
    B -->|"Mistake in syntax"| E["SyntaxError<br/>Program does not run"]
    B -->|"Success"| C["Bytecode<br/>.pyc file"]
    C --> D["PVM<br/>Python Virtual Machine"]
    D --> O["Output"]
```

**Step by step:**

1. You write the source code in a `.py` file.
2. When you run it, Python compiles it into **bytecode**. Bytecode is a simple set of instructions for the PVM, not for the real CPU.
3. The PVM reads the bytecode one instruction at a time and runs it.

You only run one command, `python hello.py`. Steps 2 and 3 happen automatically. That is why Python feels like an interpreted language even though a compile step exists inside it.

### Feature 9: Extensible

We can use programs written in **other languages** (such as C or C++) inside Python. The main advantages are:

1. We can reuse **existing legacy code** that is not written in Python.
2. We can **improve performance**: slow parts can be written in a fast language like C and called from Python.

**Example:** The NumPy library does its heavy maths in C, so Python programs that use NumPy run fast.

### Feature 10: Embedded

This is the opposite of extensible. We can put Python code **inside programs written in other languages**. In other words, we can embed Python anywhere.

**Example:** Tools like Blender (3D graphics) and many games embed Python so users can write scripts to control them.

```mermaid
flowchart LR
    subgraph EXT["Extensible"]
        direction LR
        PY1["Python program"] -->|"uses"| C1["C / C++ code"]
    end
    subgraph EMB["Embedded"]
        direction LR
        C2["C / C++ program"] -->|"uses"| PY2["Python code"]
    end
```

### Feature 11: Extensive library

Python comes with a rich built-in library, called the **standard library**. You can use it directly, so you do not need to write that functionality yourself. People often say Python comes with *"batteries included"*.

```python
# Load the math module for mathematical functions
import math

# Load the statistics module for averages and similar calculations
import statistics

# Print the square root of 144
print(math.sqrt(144))

# Print 5 factorial, which is 5 x 4 x 3 x 2 x 1
print(math.factorial(5))

# Create a list of marks
marks = [78, 85, 92, 66, 89]

# Print the average of the marks
print(statistics.mean(marks))

# Print the highest mark using the built-in max() function
print(max(marks))
```

**Output**

```text
12.0
120
82
92
```

**How this program runs:** The two `import` lines load ready-made modules. `math.sqrt()` and `math.factorial()` come from the `math` module. `statistics.mean()` adds the marks (410) and divides by the count (5) to get `82`. `max()` is built into Python, so it needs no import. We wrote no maths logic ourselves. The library did all the work.

---

## 8. Limitations of Python

No language is perfect. Python has two main limitations:

| Limitation | Why | What people do about it |
|-----------|-----|------------------------|
| **Performance is lower** than C or Java | Python is an interpreted language. The PVM runs bytecode step by step, which is slower than running native machine code. | Use libraries written in C (such as NumPy), or use PyPy (see flavors below) |
| **Not commonly used for mobile applications** | Android and iOS are built around Java/Kotlin and Swift. | Frameworks such as Kivy and BeeWare can build mobile apps in Python, but they are less common |

---

## 9. Flavors of Python

A **flavor** (also called an **implementation**) is a version of the Python software built for a particular platform or purpose. The language is the same, but the program that runs it is different.

```mermaid
flowchart TD
    P(("Python language")) --> CP["CPython<br/>Standard, written in C"]
    P --> JY["Jython / JPython<br/>Runs on the JVM"]
    P --> IP["IronPython<br/>Runs on .NET"]
    P --> PP["PyPy<br/>Faster, has a JIT compiler"]
    P --> RP["RubyPython<br/>For Ruby platforms"]
    P --> AP["Anaconda Python<br/>For large data processing"]
```

| Flavor | Built for | Key point |
|--------|-----------|-----------|
| **CPython** | C language applications | The **standard** flavor. When you download Python from python.org, you get CPython. |
| **Jython** or **JPython** | Java applications | Runs on the **JVM** (Java Virtual Machine) |
| **IronPython** | C# and the .NET platform | Works with .NET libraries |
| **PyPy** | Speed | Has a **JIT (Just In Time) compiler** inside its PVM, so programs usually run faster |
| **RubyPython** | Ruby platforms | Lets Ruby programs use Python |
| **Anaconda Python** | Large volumes of data | Specially designed for data processing. It comes with many data science libraries already installed. |

> **Note:** Strictly speaking, Anaconda is a *distribution* (CPython plus many extra libraries and tools), and RubyPython is a *bridge* between Ruby and Python. They are listed here because the notes include them.

**What is a JIT compiler?** A normal PVM runs bytecode instruction by instruction every time. A JIT compiler notices code that runs again and again (for example, inside a loop) and converts it into fast machine code while the program is running. The next time, the fast version is used. That is why PyPy is often faster than CPython.

You can check which flavor you are using:

```python
# Load the platform module, which gives details about the system
import platform

# Print the name of the Python implementation in use
print(platform.python_implementation())
```

**Output** (when run with the standard Python from python.org)

```text
CPython
```

---

## 10. Python versions

| Version | Released |
|---------|----------|
| Python 1.0 | January 1994 |
| Python 2.0 | October 2000 |
| Python 3.0 | December 2008 |

> **Important:** Python 3 is **not backward compatible** with Python 2. There is no guarantee that a Python 2 program will run in Python 3.

Two common examples of the difference:

| Code | Python 2 | Python 3 |
|------|----------|----------|
| Printing | `print "Hello"` (a statement) | `print("Hello")` (a function, brackets needed) |
| `7 / 2` | `3` (whole number division) | `3.5` (true division) |

The Python 3 behaviour:

```python
# Divide 7 by 2 with true division, which keeps the decimal part
print(7 / 2)

# Divide 7 by 2 with floor division, which drops the decimal part
print(7 // 2)
```

**Output**

```text
3.5
3
```

**Current versions:** The notes mention Python 3.6.1 and Python 2.7.13, which were current when the notes were written. Since then:

- Python 2 reached its **end of life on 1 January 2020**. It gets no more updates or security fixes. Do not use it for new work.
- Python 3 has had many new releases, with a new version every October. This course uses **Python 3.12 or newer**. Check [python.org/downloads](https://www.python.org/downloads/) for the latest version.

You can check which version you have:

```python
# Load the sys module, which gives details about the Python interpreter
import sys

# Print the major and minor version numbers
print(sys.version_info.major, sys.version_info.minor)
```

**Output** (on Python 3.12)

```text
3 12
```

---

## 11. Quick revision

| Question | Answer |
|----------|--------|
| What type of language is Python? | General purpose, high level programming language |
| Who developed Python? | Guido van Rossum |
| When and where? | 1989, at CWI (National Research Institute), Netherlands |
| Official date of birth | 20 February 1991 |
| Where does the name come from? | BBC TV show "Monty Python's Flying Circus" (1969 to 1974) |
| Functional programming features from | C |
| Object oriented features from | C++ |
| Scripting features from | Perl and Shell Script |
| Modular programming features from | Modula-3 |
| Most of the syntax from | C and ABC |
| Who runs Python bytecode? | PVM (Python Virtual Machine) |
| Dynamically typed means | No type declaration; the type comes from the assigned value |
| Main limitations | Slower performance; not common for mobile apps |
| Standard flavor | CPython |
| Flavor with a JIT compiler | PyPy |
| Is Python 3 backward compatible with Python 2? | No |

---

## 12. Practice questions

1. Explain the meaning of *general purpose* and *high level* with one example each.
2. Write the "sum of two numbers" program in Python with your own two numbers. What output do you get?
3. Python is called *dynamically typed*. Write a three-line program that proves it using `type()`.
4. What is the difference between *extensible* and *embedded*?
5. What does the PVM do? Draw the steps from a `.py` file to the output.
6. Name two limitations of Python and one way to reduce each.
7. Which flavor of Python would you choose to work with Java code? Which one for faster execution?
8. Why might a program written for Python 2 fail in Python 3? Give two examples.
9. Run `import platform` and `print(platform.python_implementation())` on your computer. What flavor do you have?

---

<p align="center">
  <a href="../README.md">Back to course home</a> &nbsp;|&nbsp; <a href="../01.1%20Setup%20and%20first%20program/README.md">Next: 01.1 Setup and first program</a>
</p>
