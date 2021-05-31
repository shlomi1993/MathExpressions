# MathExpressions

## In General

In this repo I share my imiplementation of a system that can represent nested mathematical expressions that include variables, evaluate their values for specific variable assignments, differentiate them, and simplify the results.

This implementation is based on **Object-Oriented priniples** and **Composite/Interpreter Design-Pattern**.

## The ProjectThis project is devided to three main parts:

### Part 1 -- Mathematical Expressions

In this part I created a representation for a mathematical expressions such as sin(((2x + y) * 4)^x).
I created classes for unary expressions such as:
- Var("x")
- Sin(x)
and for binary expression such as:
- Plus(x, y)
- Mul(x, y)
- Pow(x, y)

#### Mathematical Expression Representation

The idea is to represent a mathematical expression using:

Expression e = new Sin(
                     new Pow(
                        new Mul(
                           new Plus(
                              new Mul(new Num(2), new Var("x")),
                              new Var("y")),
                           new Num(4)),
                     new Var("x")))
                     
That is how we get a tree like this:
![image](https://user-images.githubusercontent.com/72878018/120223169-d6f95e00-c249-11eb-8246-da98db67fb19.png)

#### Class Hirarchy

![image](https://user-images.githubusercontent.com/72878018/120223262-03ad7580-c24a-11eb-8039-9947d1a673ed.png)


### Part 2 -- Automatic Differentitation

In this part I created a mechanism to differentiate them according to a given variable.

### 3 -- Simplification

The representation of the mathematical expression is saturated with parenthesis.
This part is about simplify the representation by reducing the number of parenthesis.

## Language

- 100% Java.

## IDEs, Writers and tools

1. JetBrains IntelliJ IDEA
2. Notepad++
3. CheckStyle - for maintaining Java coding convention.
