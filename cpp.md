**C++ Interview Questions and Answers**

---

**1. What is encapsulation and how can we achieve data encapsulation in C++?**

> **Encapsulation** is the process of **wrapping data and functions** into a single unit called a class. It helps to **protect the data** from outside interference and misuse.
>
> We achieve encapsulation by making the class **data members private** and providing **public getter and setter functions** to access and update those data members.

```cpp
class Student {
private:
    int marks;

public:
    void setMarks(int m) {
        marks = m;
    }

    int getMarks() {
        return marks;
    }
};
```

---

**2. Which methodology is used for code reusability?**

> The answer is **Inheritance**.
>
> Inheritance allows a class (child) to reuse the properties and behavior (functions) of another class (parent), thereby promoting **code reusability**.

---

**3. Which methodology among these helps with readability?**

> The methodology that improves **readability** is **Encapsulation**.
>
> By hiding internal details and exposing only what is necessary, encapsulation makes the code more **organized, clean, and easier to understand**.

---

**4. What is a class and an object?**

> A **class** is a blueprint for creating objects. It defines data members and functions. An **object** is an instance of a class. It has real memory allocated.

```cpp
class Car {
public:
    void drive() {
        cout << "Driving..." << endl;
    }
};

int main() {
    Car myCar; // Object
    myCar.drive();
    return 0;
}
```

---

**5. What are class members and what access control can we use?**

> Class members include **data members (variables)** and **member functions (methods)**. Access control keywords in C++:
>
> - `public`: Accessible from anywhere
> - `private`: Accessible only within the class
> - `protected`: Accessible in the class and derived classes

---

**6. What is the purpose of a constructor and when is it called?**

> A **constructor** is a special function that has the same name as the class. It is used to **initialize objects** when they are created.
>
> It is **automatically called** when an object is instantiated.

```cpp
class Person {
public:
    Person() {   // Constructor
        cout << "Constructor called" << endl;
    }
};
```

---

**7. What is public, private, and protected inheritance?**

| Type      | Base Public | Base Protected | Base Private  |
| --------- | ----------- | -------------- | ------------- |
| public    | public      | protected      | not inherited |
| protected | protected   | protected      | not inherited |
| private   | private     | private        | not inherited |

> - **Public Inheritance**: Derived class publicly inherits base class features
> - **Protected Inheritance**: Base members become protected in derived class
> - **Private Inheritance**: Base members become private in derived class

---

**8. How can we achieve inheritance in C++? Which operator is used?**

> We achieve inheritance using the **colon (**\`\`**) operator** with access specifier.

```cpp
class Base {
    // ...
};

class Derived : public Base {
    // Inherits from Base
};
```

---

**9. What is base class and derived class?**

> A **base class** is the class being inherited from. A **derived class** is the class that inherits.

```cpp
class Animal {  // Base class
public:
    void eat() {
        cout << "Eating..." << endl;
    }
};

class Dog : public Animal {  // Derived class
public:
    void bark() {
        cout << "Barking..." << endl;
    }
};
```

---

**10. What is the difference between overriding and overloading?**

| Feature    | Overloading               | Overriding                  |
| ---------- | ------------------------- | --------------------------- |
| Location   | Same class                | Base and derived class      |
| Parameters | Must differ               | Must match exactly          |
| Purpose    | Compile-time polymorphism | Runtime polymorphism        |
| Keyword    | No keyword needed         | Use `virtual` in base class |

---

**11. What are the advantages of operator overloading?**

> - Makes code **easier to read and write**
> - Allows operators to work with **user-defined types**
> - Increases **code clarity** and **intuitiveness**

```cpp
class Complex {
    int real, imag;
public:
    Complex(int r, int i) : real(r), imag(i) {}
    Complex operator + (const Complex& c) {
        return Complex(real + c.real, imag + c.imag);
    }
};
```

---

**12. Syntax of creating a class template**

```cpp
template <class T>
class MyClass {
    T value;
public:
    MyClass(T v) : value(v) {}
    void show() {
        cout << "Value: " << value << endl;
    }
};
```

---

**13. Difference between virtual and pure virtual function**

| Feature               | Virtual Function  | Pure Virtual Function           |
| --------------------- | ----------------- | ------------------------------- |
| Has definition        | Yes               | No (only declared with `= 0`)   |
| Must be overridden?   | No                | Yes                             |
| Makes class abstract? | No                | Yes                             |
| Use                   | Optional override | Force derived class to override |

```cpp
class Base {
public:
    virtual void show() { cout << "Base"; }        // Virtual
    virtual void print() = 0;                      // Pure virtual
};
```

---

**14. If a class has at least one pure virtual function, what type of class is it?**

> If a class has at least one pure virtual function, it becomes an **abstract class**.
>
> Abstract classes **cannot be instantiated**, and are used as **base classes only**.

---

**15. In exception handling, which block executes when an exception is thrown?**

> When an exception is thrown, the **matching ****\`\`**** block** executes. The `try` block is interrupted, and control goes to the corresponding `catch` block.

```cpp
try {
    throw 10;
} catch (int e) {
    cout << "Caught exception: " << e;
}
```

---

**16. What is the purpose of ****\`\`**** keyword in C++?**

> The `throw` keyword is used to **raise an exception** manually. It transfers control to the matching `catch` block.

```cpp
if (b == 0)
    throw "Divide by zero error";
```

---

**17. Header file used for input/output in C++**

> The header file used for input/output is \`\`.
>
> It provides `cin`, `cout`, `cerr`, and `clog`.

```cpp
#include <iostream>
using namespace std;
```

