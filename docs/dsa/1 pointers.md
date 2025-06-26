---
id: pointers
title: Pointers in C++
sidebar_label: Pointers
description: Understand pointers with simple C++ examples and use-cases.
slug: /dsa/pointers
---

> “A pointer is a variable that stores the address of another variable.”

---
## 🧠 Why Learn Pointers?

- Core to memory management
- Essential for arrays, linked lists, trees
- Enables efficient parameter passing

---

## 🧪 Example: Pointer Basics

```cpp
int x = 5;
int* ptr = &x;
cout << "x = " << x << ", *ptr = " << *ptr << ", &x = " << &x;
```