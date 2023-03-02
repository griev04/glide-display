+++
title = "Lombok"
description = "Project Lombok"
outputs = ["Reveal"]

[reveal_hugo]
custom_css = "css/custom.css"
+++

# Lombok

---

{{%fragment%}}### Lombok{{%/fragment%}}

{{%fragment%}}#### Indonesia{{%/fragment%}}


<img src="img/lombok-island.jpg" alt="Lombok Island, Indonesia">

---

{{%fragment%}}### Not as good{{%/fragment%}}

<img src="img/lombok-chili.webp" alt="Lombok Project">

{{%fragment%}}#### But still cute{{%/fragment%}}

---

## Issue
Java is a very verbose language with a lot of boilerplate code that clutters your business logic and IDE.

Most of this code is repeated and brings no value to your project.

---

## What if

we could avoid all this boilerplate by using some `annotations`?

{{%fragment%}}
### Enter `Project Lombok`
{{%/fragment%}}

---

## Lombok
Lombok is an annotation-based Java library, enabling you to minimize redundant code.

{{%fragment%}}
It includes a range of annotations designed to eliminate the need for commonly used Java code that can be tedious, repetitive, or verbose.
{{%/fragment%}}

---

### Great but what does it mean exactly?

{{%fragment%}}
With Lombok, you can avoid composing constructors, implementing the toString(), equals(), and hashCode() methods, among other things, by merely incorporating a few annotations.
{{%/fragment%}}

---

### How does it work?

Lombok works by using annotations to automatically generate code during compilation. 

{{%fragment%}}
When an annotation in your Java code is met, it instructs the Lombok compiler to magically generate some boilerplate for you. 
{{%/fragment%}}

{{%fragment%}}
This generated code is then compiled along with your source code, and the resulting class file contains the code from both sources.
{{%/fragment%}}