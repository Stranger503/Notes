---
title: Sicp Notes
author: "Mohammed Shahid"
fontfamily: libertine
fontsize: 12pt
documentclass: article
classoption: a4paper
output: pdf_document
---
**Prefix Notation**:Placing an operator to the left of the operands.

**Advantages**:

1. It can take any number of arguments for a procedure.
```{scheme}
(+ 10 23 88 123 908)
1152
```
2. No Ambiguity can arise because the operator is always the leftmost element and the entire combination is delimited by the parentheses.
3. A second advantage of prefix notation is that it extends in a straightforward way to allow combinations to be nested, that is, to have combinations whose elements are themselves combinations:

```{scheme}
(+ (* 3 5) (- 10 6))
19
```
4. There is no limit (in principle) to the depth of such nesting and to the overall complexity of the expressions that the Lisp interpreter can evaluate.
5. It is we humans who get confused by still relatively simple expressions such as

```{scheme}
(+ (* 3 (+ (* 2 4) (+ 3 5))) (+ (- 10 7) 6))
```


## 1.1.2 Naming and Environments

*  The name identifies a variable whose value is the object.
__(define name "shahid")__
* The interpreter must maintain some sort of memory that keeps track of the name-object pairs. This memory is called the environment (more precisely the global environment
