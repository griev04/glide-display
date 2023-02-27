+++
title = "Lombok"
description = "Project Lombok"
outputs = ["Reveal"]

[reveal_hugo]


+++

# Project Lombok

---

### Lombok, Indonesia

<img src="lombok-island.jpg" alt="Lombok Island, Indonesia">

---

<img src="lombok-chili.webp" alt="Lombok Project">

---

## Issue
Java is a very verbose language with a lot of boilerplate code that clutters your business logic and IDE.
Most of this code is repeated and brings no value to your project.

---

## What if

we could avoid all this boilerplate by using some `annotations`?

{{%fragment%}}
Enter `Project Lombok`
{{%/fragment%}}

---

## Lombok
Lombok is an annotation-based Java library, enabling you to minimize redundant code. The library includes a range of annotations designed to eliminate the need for commonly used Java code that can be tedious, repetitive, or verbose.

---

### Great but what does it mean exactly?

{{%fragment%}}
With Lombok, you can avoid composing constructors without arguments, implementing the toString(), equals(), and hashCode() methods, among other things, by merely incorporating a few annotations.
{{%/fragment%}}

---

### How does it workd bts?

This Java library provides you with several annotations aimed at avoiding writing Java code known to be repetitive and/or boilerplate. Project Lombok works by plugging into your build process. Then, it will auto-generate the Java bytecode into your .class files required to implement the desired behavior, based on the annotations you used.
Lombok works by using annotations to generate code automatically during compilation. When you use a Lombok annotation in your Java code, it tells the Lombok compiler to generate some boilerplate code automatically for you. This generated code is then compiled along with your source code, and the resulting class file contains the code from both sources.

---

### Missing
- Data
- Value
- Advanced
- Builder

Sources:
- https://projectlombok.org/features/
- https://auth0.com/blog/a-complete-guide-to-lombok/
- https://www.baeldung.com/intro-to-project-lombok
