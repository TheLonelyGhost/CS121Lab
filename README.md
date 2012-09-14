CS121 - Lab 4
=============

**Date:** 2012-09-13

# Synopsis #

Master the Postfix Notation and Use Stacks for Evaluation.

## Introduction ##

It is important for us to be comfortable using postfix notation in Computer Science. So today, we will:

- Clarify the right way to evaluate a postfix expression,
- Practice pushing, popping, and evaluating a postfix expression in MS Word,
- Run our author's `StackDemo` in Eclipse, and
- Evaluate some postfix expressions using our author's `PostFixEvaluator in Eclipse.

Sections 1 and 3 are just FYI.

Sections 2 and 4 contain yellow boxes you much type answers in that will be graded at the end of the lab.

# 1. Postfix Expressions #

"Traditionally, arithmetic expressions are written in ***infix*** notation, meaning that the operator is placed between the operands (numbers) in the form."

```
<operand1>		<operator>		<operand2>
```

such as the expression `9 - 6`.

However, "a **postfix** expression is generally easier to evaluate than an *infix* expression because the precedence rules and parentheses do not have to be taken into account" (Lewis &amp; Chase, p. 44). A postfix expression has the form

```
<operand1>		<operand2>		<operator>
```

such as the expression `9 6 -` which is equivalent to the infix notation `9 - 6`. Notice that the operator is simply moved in between the operands (numbers). Take a minute to read and understand the more complicated example given on page 45 of our text. Ask a lab assistant if you have any question with it.

## Using the Stack ##

It turns out that a **stack** is the perfect collection to use for evaluating postfix expressions.

**FIGURE 3.7:**

```
7 4 -3 * 1 5 + / *
```

In the fourth update of the stack, the next operator encountered is the division symbol `/` with the operands 6 and -12. The proper way to pop these off the stack and evaluate them follows:

- Pop the 6 off the top of the stack and store as `<operand2>`
- Pop the -12 off the top of the stack and store as `<operand1>`

Now we have clarified using the stack to evaluate postfix expressions.

# 2. Practice pushing, popping, and evaluating in MS Word #

Evaluate some expressions by using Tables to show how the stack changes after each operation. Fill the result cell with yellow shading as shown in the attached document (`CS121 - Lab 04 - Handout.docx`).

# 3. Run `StackDemo` in Eclipse #

1. Download **Lab 4 Files** folder from the repository, saving it to the desktop.
2. 