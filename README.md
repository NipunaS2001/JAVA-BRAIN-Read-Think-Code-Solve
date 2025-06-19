# JAVA BRAIN-Read-Think-Code-Solve

<h1># Java Primitive Data Types</h1>

## What are Primitive Data Types?

Think of **primitive data types** as the fundamental building blocks of Java programming – like LEGO blocks that you use to build bigger, more complex things. They are the simplest, most basic types of data you can work with in Java. These types are built into the language itself, not created by the programmer.

---

## The 8 Primitive Types (Like Different Sized Boxes)

### Numbers with No Decimals (**Integers**)

- **int** – Regular numbers like `42`, `-15`, `1000` (most common)
- **byte** – Very small numbers (`-128` to `127`)
- **short** – Small numbers (`-32,768` to `32,767`)
- **long** – Very big numbers (add `'L'` at end: `123456789L`)

### Numbers with Decimals

- **double** – Decimal numbers like `3.14`, `-2.5` (**most common for decimals**)
- **float** – Less precise decimals (add `'f'` at end: `3.14f`)

### Other Types

- **char** – Single characters like `'A'`, `'5'`, `'@'`
- **boolean** – Only `true` or `false` (yes/no)

---

## Simple Examples

```java
// Different types of data
int age = 25;                    // Whole number
double price = 19.99;            // Number with decimal
char grade = 'A';                // Single character
boolean isStudent = true;        // true or false
```

---

## Why Use Different Types?

Think of it like choosing the right container for what you want to store:

- You **wouldn’t use a huge truck to deliver a letter** (waste of space)
- You **wouldn’t use a small envelope to ship a TV** (won’t fit)

```java
byte smallNumber = 10;        // Small container for small number
int regularNumber = 50000;    // Regular container for regular number
```

---

## Key Points

### 1. They Save Memory

- `int` uses less computer memory than storing numbers as text.
- Like using a small box instead of a big box for small items.

### 2. They're Fast

- Computer can do math with primitives very quickly.
- Like using a calculator instead of counting on fingers.

### 3. No Null Values

- Primitives **always have a value** (never "empty").
- `int` starts at `0`, `boolean` starts at `false`.

### 4. Type Conversion

```java
int smallBox = 10;
long bigBox = smallBox;      // OK - putting small thing in big box

long bigNumber = 1000;
int smallBox = bigNumber;    // ERROR - can't fit big thing in small box
int forced = (int) bigNumber; // OK - but might lose data (forcing it)
```

---

## Common Mistakes

### 1. Using Wrong Size

```java
byte tinyNumber = 200;  // ERROR! 200 is too big for byte (max 127)
int goodNumber = 200;   // OK - int can hold 200
```

### 2. Forgetting Decimal Point

```java
double price = 10;      // OK - becomes 10.0
double price = 10.50;   // Better - clearly shows it's decimal
```

### 3. Character vs String Confusion

```java
char singleLetter = 'A';        // Single quotes for ONE character
String manyLetters = "Hello";   // Double quotes for WORDS
```

---

## Memory Usage (Like Box Sizes)

| Type    | Memory Size  | What It's Good For                |
|---------|--------------|-----------------------------------|
| byte    | Tiny box     | Ages, small counters              |
| int     | Medium box   | Most whole numbers                |
| long    | Big box      | Very large numbers                |
| double  | Medium box   | Prices, measurements              |
| char    | Small box    | Single letters/symbols            |
| boolean | Tiny box     | Yes/No questions                  |

---

## Practical Examples 

```java
// Student information system
int studentAge = 20;
double gpa = 3.75;
char letterGrade = 'B';
boolean isGraduated = false;
byte numberOfClasses = 5;

// Simple calculator
int firstNumber = 10;
int secondNumber = 5;
int sum = firstNumber + secondNumber;        // 15
double average = sum / 2.0;                  // 7.5
```

---

## When You Get More Advanced

Later, you'll learn about:

- **Wrapper Classes** (`Integer`, `Double`, etc.) – like gift boxes around primitives
- **Collections** (Lists, Maps) – which need wrapper classes
- **Performance optimization** – when primitives make your program faster

---

## Remember This!

- **Start simple** – use `int` for whole numbers, `double` for decimals
- **Choose the right size** – don’t use `long` if `int` works fine
- **Primitives are fast and efficient** – perfect for math and counters
- **They always have values** – never worry about them being "empty"

---

> Think of primitives as your **basic tools** – like having a hammer, screwdriver, and wrench. You’ll use them in almost every Java program you write!

---

## 🎉 Bonus: Quick Reference Table

| Data Type | Example Value | Range / Size                | Typical Use Case        |
|-----------|--------------|-----------------------------|------------------------|
| byte      | 127          | -128 to 127 (1 byte)        | Small counters, flags  |
| short     | 32000        | -32,768 to 32,767 (2 bytes) | Medium-size numbers    |
| int       | 100000       | -2B to 2B (4 bytes)         | Most whole numbers     |
| long      | 5_000_000L   | Huge! (8 bytes)             | Big counts, timestamps |
| float     | 3.14f        | 6-7 decimal digits (4 bytes)| Approximate decimals   |
| double    | 2.71828      | 15 decimal digits (8 bytes) | Precise decimals       |
| char      | 'Z'          | Unicode character (2 bytes) | Single letters/symbols |
| boolean   | true         | true/false (1 bit/byte)     | Yes/No flags           |

---

## 🏆 Declaration Summary

- **Declare** variables using the type, then the name, then the value:
  ```java
  int score = 100;
  double price = 19.99;
  char symbol = '@';
  boolean isActive = false;
  ```

---



---

<h1># 📘 Java Variables</h1>

---

## **1. Definitions & Concepts**

### 🔹 What is a Variable in Java?

A **variable** in Java is a named memory location that stores a value. Variables allow programs to store, retrieve, and manipulate data dynamically during execution.

```java
int age = 25;
```

Here, `age` is a variable holding the value `25`.

### 🔹 Why are Variables Essential?

* Store information temporarily.
* Enable logic: calculations, decisions, loops.
* Make code flexible and reusable.

### 🔹 Types of Variables (By Behavior)

* **Primitive variables:** Hold actual values like numbers, characters, booleans.
* **Reference variables:** Store memory addresses of objects (arrays, custom classes, etc.).

### 🔹 Definitions

* **Identifier:** The name of a variable (e.g., `age`, `price`). Must follow naming rules.
* **Literal:** The fixed value assigned to a variable (e.g., `25` in `int age = 25;`).
* **Keyword:** Reserved words like `int`, `final`, `static` that can't be used as variable names.

---

## **2. Variable Categories**

### 2.1 📍 **Local Variables**

* Declared **inside** methods, constructors, or blocks.
* **No default value** → must be explicitly initialized before use.
* Scope = the block they're declared in.

```java
void greet() {
    String name = "Nipuna";
    System.out.println("Hello " + name);
}
```

### 2.2 🧍 **Instance (Non-Static) Variables**

* Declared inside a class, **but outside any method**.
* Belong to each object.
* Automatically get default values.

```java
public class User {
    String name;    // instance variable
    int age;        // instance variable
}
```

### 2.3 🏛️ **Static (Class) Variables**

* Declared using `static`.
* Shared across **all** instances.
* Initialized at class loading time.

```java
public class Counter {
    public static int count = 0;
}
```

### 2.4 🛡️ **Constants (`final` Variables)**

* Declared using `final`.
* Value can't be changed after assignment.

```java
public static final double PI = 3.14159;
```

* **Compile-time final:** assigned immediately.
* **Runtime final:** assigned in constructor or block.

---

## **3. Data Types & Memory**

### 3.1 ⚙️ Primitive Data Types

| Type    | Size    | Range                | Default  |
| ------- | ------- | -------------------- | -------- |
| byte    | 8 bits  | -128 to 127          | 0        |
| short   | 16 bits | -32,768 to 32,767    | 0        |
| int     | 32 bits | -2^31 to 2^31-1      | 0        |
| long    | 64 bits | -2^63 to 2^63-1      | 0L       |
| float   | 32 bits | \~6-7 decimal digits | 0.0f     |
| double  | 64 bits | \~15 decimal digits  | 0.0d     |
| char    | 16 bits | '\u0000' to '\uffff' | '\u0000' |
| boolean | \~1 bit | true / false         | false    |

⚠️ Use `int` by default. Use `long` if you need big integers.

### 3.2 🧠 Reference Types

* Variables that hold references to **objects**.
* Includes custom objects, arrays, `String`, etc.
* Default = `null`.

```java
String message = "Hello";
int[] nums = {1, 2, 3};
```

* Stored in **heap memory**, while reference itself is on the **stack**.

⚠️ Accessing null references → `NullPointerException`.

---

## **4. Declaration & Initialization**

```java
int a;            // declaration
a = 5;            // initialization
int b = 10;       // declaration + initialization
```

### 🔁 Multiple Declarations

```java
int x = 1, y = 2, z;
```

### ➰ Chained Assignments

```java
int a, b, c;
a = b = c = 10;  // All variables get 10
```

### 🧩 Default Initialization

* **Fields (instance/static):** Automatically initialized.
* **Local variables:** ❌ Must be initialized manually.

---

## **5. Scope & Lifetime**

| Type     | Scope               | Lifetime                |
| -------- | ------------------- | ----------------------- |
| Local    | Inside method/block | Until block exits       |
| Instance | Whole object        | As long as object lives |
| Static   | Class-wide          | Until JVM unloads class |

### 🧱 Block Scope

```java
{
    int x = 5;
}
// x no longer exists here
```

### 🔍 Variable Shadowing

```java
int x = 10;
void test() {
    int x = 5;   // shadows outer x
    System.out.println(x); // prints 5
}
```

✅ Use `this.x` to refer to class variable.

---

## **6. Access Modifiers**

| Modifier    | Accessible From         |
| ----------- | ----------------------- |
| `public`    | Anywhere                |
| `private`   | Only inside class       |
| `protected` | Same package + subclass |
| Default     | Same package only       |

Example:

```java
public class Student {
    private int id;    // only accessible within Student class
}
```

---

## **7. Default Values**

| Type      | Default Value |
| --------- | ------------- |
| int, byte | 0             |
| float     | 0.0f          |
| boolean   | false         |
| char      | '\u0000'      |
| Object    | null          |

⚠️ **Local variables have no default values!**

---

## **8. Memory Allocation**

| Variable Type | Stored In   |
| ------------- | ----------- |
| Local         | Stack       |
| Instance      | Heap        |
| Static        | Method Area |

* **Garbage Collector** cleans up unused heap objects.
* Reference variables → eligible for GC when not referenced.

---

## **9. Naming Conventions**

✅ Follow these best practices:

* camelCase for variables: `userName`, `totalCount`
* UPPER\_CASE for constants: `MAX_VALUE`
* Avoid keywords: ❌ `int class = 5;`
* Avoid meaningless names: ❌ `x1`, ✅ `totalPrice`

---

## **10. Modifiers & Qualifiers**

### 🔐 `final`

* Makes a variable **constant**.
* Must be initialized once.

```java
final int MAX_USERS = 100;
```

### 🌐 `transient`

* Used in serialization. JVM **ignores** it when saving objects.

```java
transient String password;
```

### 🔁 `volatile`

* Prevents thread caching—used in multithreading.

```java
volatile boolean flag = true;
```

---

## **11. Common Pitfalls**

⚠️ Uninitialized Local Variable

```java
int x;
System.out.println(x);  // ❌ Compile-time error
```

⚠️ Integer Overflow

```java
int max = Integer.MAX_VALUE;
int result = max + 1;  // wraps to negative
```

⚠️ String Comparison

```java
String a = "hello";
String b = new String("hello");

System.out.println(a == b);      // false
System.out.println(a.equals(b)); // true ✅
```

---

## **12. Practical Examples**

### ✅ Local Variable

```java
void calculate() {
    int a = 10, b = 20;
    int sum = a + b;
    System.out.println(sum);
}
```

### ✅ Instance vs Static

```java
class Counter {
    static int totalCount = 0;
    int instanceCount = 0;

    Counter() {
        totalCount++;
        instanceCount++;
    }
}
```

### ✅ Final Variable

```java
public class MathConstants {
    public static final double PI = 3.14159265359;
}
```

### ⚠️ Shadowing

```java
public void setX(int x) {
    x = x;           // ❌ no effect
}

public void setXCorrect(int x) {
    this.x = x;      // ✅ modifies the instance variable
}
```

---

## **13. Exercises & Mini-Projects**

### 📝 Exercise 1: `Product` Class

Create a class with private fields, getters, and constructor:

```java
public class Product {
    private int id;
    private String name;
    private double price;

    public Product() {
        System.out.println(id + " " + name + " " + price); // defaults
    }
}
```

### 🧮 Exercise 2: `MathUtils` Constants

```java
public class MathUtils {
    public static final double PI = 3.14159;

    public static double areaOfCircle(double r) {
        return PI * r * r;
    }
}
```

### 🔁 Exercise 3: Swap

```java
void swap(int a, int b) {
    int temp = a;
    a = b;
    b = temp;
    System.out.println(a + " " + b); // only inside method
}
```

Use wrapper like `AtomicInteger` or return array to “swap.”

---

### 💼 Mini Project: BankAccount

```java
public class BankAccount {
    private String accountNumber;
    private String accountHolder;
    private double balance;
    public static double interestRate = 0.05;

    public void deposit(double amt) {
        balance += amt;
    }

    public void applyInterest() {
        balance += balance * interestRate;
    }
}
```

---

## **14. Advanced Topics**

### 📌 Default Values for Arrays

```java
int[] nums = new int[5];   // all elements = 0
String[] names = new String[5]; // all elements = null
```

### 🔄 Auto-boxing/Unboxing

```java
Integer a = 10;   // auto-boxing
int b = a;        // unboxing
```

⚠️ `Integer i = null; int j = i;` → `NullPointerException`

### 🚀 Escape Analysis

* JVM may allocate short-lived objects on the **stack**.
* Helps optimize memory & GC.

### 💡 `var` (Java 10+)

```java
var message = "Hi"; // inferred as String
```

✅ Good for short scopes. Avoid in public APIs.

---

## **15. Debugging Tips**

* ✅ Always initialize local variables.
* ✅ Use constants instead of magic numbers.
* ✅ Prefer `equals()` for object comparison.
* ✅ Guard against nulls: `if (s != null && !s.isEmpty())`
* ✅ Be careful with unboxing nulls: `Integer i = null; int x = i;` → ❌

---

# ✅ Summary: Your Mastery Checklist

| ✔️ Mastered Topic                         |
| ----------------------------------------- |
| ✅ Variable types: local, instance, static |
| ✅ Primitive vs Reference                  |
| ✅ Default values & memory model           |
| ✅ Final variables and constants           |
| ✅ Scope, shadowing, and access modifiers  |
| ✅ JVM memory behavior for variables       |
| ✅ Common pitfalls and how to avoid them   |
| ✅ Real-world exercises and projects       |

---


<br>


📘 Java Literals 
Including memory usage, internal workings, and best practices

📖 Table of Contents
What Are Literals?

Types of Java Literals

Integer Literals

Floating-point Literals

Character Literals

String Literals

Boolean Literals

Null Literal

How Java Stores Literals (Memory Use)

Behind the Scenes (JVM Behavior)

Escape Sequences in Literals

Common Errors and Pitfalls

Cheat Sheet + Practice Questions

🧩 1. What Are Java Literals?
A literal is a fixed value assigned to a variable. It's the actual data in the code.

java
Copy
Edit
int age = 25;        // 25 is a literal
boolean isOpen = true; // true is a literal
✅ You use literals whenever you write a value directly in your code.

🧪 2. Types of Java Literals
1️⃣ Integer Literals
Used for whole numbers.

java
Copy
Edit
int x = 10;
long y = 100000L;  // 'L' indicates long
Allowed Bases:
Decimal (base 10): 123

Octal (base 8): 0123 → starts with 0

Hexadecimal (base 16): 0x7B

Binary (base 2): 0b1010

📦 Memory Use:

byte → 1 byte

short → 2 bytes

int → 4 bytes

long → 8 bytes

2️⃣ Floating-Point Literals
Used for numbers with decimals.

java
Copy
Edit
float pi = 3.14f;     // 'f' or 'F' must be used for float
double gravity = 9.8; // double is default
📦 Memory Use:

float → 4 bytes (32-bit IEEE 754)

double → 8 bytes (64-bit IEEE 754)

🧠 How It Works Internally:

Uses IEEE 754 standard

Stores number in sign + exponent + mantissa format

3️⃣ Character Literals
Used for single characters.

java
Copy
Edit
char letter = 'A';
char unicodeChar = '\u0041';  // Unicode representation
📦 Memory Use:

char uses 2 bytes, stores Unicode value (0–65535)

✅ Character literal must be enclosed in single quotes 'A'

4️⃣ String Literals
Used for sequences of characters.

java
Copy
Edit
String name = "Nilasi";
Stored in String Pool (in the heap memory)

Strings are immutable — can’t be changed after creation

📦 Memory Use:

Depends on the length and characters (each char = 2 bytes)

5️⃣ Boolean Literals
java
Copy
Edit
boolean isTrue = true;
boolean isFalse = false;
Only two values: true, false

Stored as 1 byte in most JVMs

6️⃣ Null Literal
Used to denote no object.

java
Copy
Edit
String name = null;
null is not the same as empty ("")

Indicates that the reference doesn’t point to any object

🧠 3. How Java Stores Literals (Memory)
Literal Type	Stored In	Memory Use
int, float	Stack	Fixed size
char, boolean	Stack	Fixed size
String	Heap (String Pool)	Variable size
null	Stack reference	No object

⚙️ 4. Behind the Scenes (BTS) – How JVM Handles Literals
🔍 When you write:
java
Copy
Edit
int x = 5;
📦 JVM does:

Allocates 4 bytes in stack memory

Stores value 5 in binary (0000 0101)

🔍 When you write:
java
Copy
Edit
String s1 = "hello";
String s2 = "hello";
📦 JVM:

Puts "hello" in String pool

Both s1 and s2 point to the same memory (to save space)

🧠 JVM optimizes literals for performance and memory

🧵 5. Escape Sequences in Literals
Used in char or String literals for special characters:

Sequence	Meaning
\n	New line
\t	Tab
\\	Backslash
\"	Double quote
\'	Single quote

java
Copy
Edit
System.out.println("Name:\tNilasi\nStatus:\tStudent");
⚠️ 6. Common Errors with Literals
Error	Reason
char c = "A";	Wrong quotes. Use single: 'A'
float x = 3.14;	Must use f like: 3.14f
int x = 123456789012345;	Too large. Use long and add L
String s = null; s.length()	NullPointerException

📌 7. Java Literal Cheat Sheet
Type	Literal Example	Notes
int	100, 0x7F, 0b1101	Default for integers
long	100000L	Use L at end
float	3.14f	Must use f
double	3.14, 1.0e10	Default for decimal values
char	'A', '\n'	Single character or escape
String	"Java"	Stored in heap/String pool
boolean	true, false	Only two options
null	null	For reference types only

🧪 Practice Section
✅ Task 1: Identify literal types
java
Copy
Edit
int a = 10;
char c = 'B';
String name = "Java";
float f = 3.5f;
boolean b = true;
✅ Task 2: Declare one variable of each type with a literal value.
🏁 Conclusion
Literals in Java are the foundation of working with variables and memory.
By mastering them, you understand:

How memory is allocated

How data is represented behind the scenes

How to write bug-free, efficient code


