CS121 - Lab 2
=============

**Date:** 2012-08-27

# Synopsis #

I need you to write a console Java program that translates a letter grade into a number grade. Letter grades are the usual: A B C D F, possibly followed by a + or -. Their numeric values are 4, 3, 2, 1, and 0, respectively. There is no F+ or F-. A *plus sign* increases the numeric value by 0.3, whereas a *minus sign* decreases it by 0.3. Input of A+ has the value 4.0. All other inputs have value -1.

## Examples ##
```
output:      Enter a letter grade:
input:       B-
output:      Numeric value:  2.7
```

```
output:      Enter a letter grade:
input:       F-
output:      Numeric value:  -1
```

# Today's Challenge Uses #

- Classes, Objects, and Methods
- Constructors
- Data Encapsulation
- Input from the Command Line
- Relational Operators
- Decision Constructs (if statements)
- Strings

# Getting Started #

1. Create a Project in Eclipse called **CS121-lab02-grade**.
2. Create a new class file called `Grade` in your project.
3. Download the `GradePrinter` class file from Blackboard and add it to the project. Notice that it instantiates an object `g` from a `Grade` class. You will be writing the `Grade` class, and upon finishing, `GradePrinter` will use it.

# Tips #

To meet this challenge, you could put the following in your **Grade** class:

- a private string `letterGrade`
- a constructor for `Grade` with an explicit parameter `String grade` that assigns that parameter to the class' `letterGrade`.
- a `getLetterGrade` method that simply returns the `letterGrade`
- a `getNumericGrade` method that
    - stores the first character of `letterGrade` into a variable,
    - checks to see if there is another character in `letterGrade`, and if so store it in another variable,
        - then evaluates to see if it is a "+", "-", and if so, assign the appropriate value to a new double variable.
    - converts the first character of `letterGrade`, the letter, into its appropriate value. Remember if there is no letter match, return -1;
    - computes the numeric grade (i.e., grade value plus modifier value)
    - ensures that an A+ shows up as 4.0 and not 4.3
    - returns the value you derive from the incoming `grade` (this will be a `double`).

# Grading #

Review the following and then call a lab assistant over to check and grade your work as follows:

- 5pts     Ensure there are no build errors.
- 5pts     Ensure you have semantically solved the problem requested.
- 10pts    Confirm the output from all possible input.
- 5pts     Clean up indentation as necessary.