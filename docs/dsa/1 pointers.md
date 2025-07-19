---
id: pointers
title: Pointers in C++
sidebar_label: 1. Pointers
description: Understand pointers with simple C++ examples and use-cases.
slug: /dsa/pointers
---

## Introduction
> “A pointer is a variable that stores the address of another variable.”

🧠 **Why Learn Pointers?**

- Core to memory management
- Essential for arrays, linked lists, trees
- Enables efficient parameter passing

---

📝**Operators : & (Address of),\*(Value Of)**
 - "&" Operator : Gives address of the variable
 - "*" Operator : Gives value of the variable

For example
```cpp
int x = 5;
int* p = &x;
cout << "Value of x = " << x << endl;
cout << "Value of p = " << *p << endl;
cout << "Address of x = " << p << endl;
cout << "Address of x = " << &x << endl;
```

💡**Good Practice**
Always assign pointer variables an address value or make it a null pointer. 

Say : 
```cpp
int* p;  // This will hold a garbage address value
(*p)++;
```
> Pointer variable "p" will hold a garbage address value and increment it. This might break the system.

Thus as a correct practice either assign an address to it on declaration, or make it a null pointer

```cpp
int *p = &x;
int *q = 0;  // Null Pointer. (*p)++ will give Segmentation Fault here.
```

## Pointer Arithmetic
<add a small lesson here>