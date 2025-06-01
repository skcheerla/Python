# Expressions in Python

In Python, an **expression** is a combination of values, variables, operators, and function calls that the Python interpreter evaluates to produce a single value. Essentially, anything that can be evaluated to a result is an expression.

Here's a breakdown of what constitutes an expression and common types of expressions in Python:

## Core Components of Expressions:

* **Literals:** These are raw data values.
    * Numbers: `5`, `3.14`, `100`
    * Strings: `"hello"`, `'Python'`
    * Booleans: `True`, `False`
    * `None`
* **Variables (Identifiers):** Names that refer to values stored in memory. When a variable is used in an expression, its current value is retrieved and used in the evaluation.
    * `x`, `name`, `total_price`
* **Operators:** Symbols that perform operations on operands.
    * **Arithmetic Operators:** `+`, `-`, `*`, `/`, `//` (floor division), `%` (modulo), `**` (exponentiation)
 
    * **Comparison (Relational) Operators:** `==` (equal to), `!=` (not equal to), `<`, `>`, `<=`, `>=`
**Logical Operators:** `and`, `or`, `not`
**Bitwise Operators:** &, |, ^, ~, <<, >>
**Assignment Operators:** =, +=, -=, etc. (While assignments themselves are statements, the right-hand side of an assignment is an expression).
Identity Operators: is, is not
Membership Operators: in, not in
Function Calls: Invoking a function, which then returns a value.
len("Python"), abs(-10), my_function(arg1, arg2)
Parentheses (): Used to group expressions and control the order of evaluation (operator precedence).
    ...

## Examples of Expressions:

* **Arithmetic Expressions:**
    ```python
    5 + 3           # Evaluates to 8
    (10 * 2) - 4    # Evaluates to 16
    x / y           # Evaluates to the result of division
    ```
    ...

## Expressions vs. Statements:

It's important to distinguish between expressions and statements in Python:

* **Expressions:** Evaluate to a value. They can be part of larger statements.
    * `5 + 3`
    * `len("hello")`
* **Statements:** Perform an action. They do not necessarily produce a value (though some statements might contain expressions that do).
    * `x = 10` (Assignment statement)
    ...
