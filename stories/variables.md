# Using variables

In ink, variables are created using the keyword `VAR` (all uppercase) followed by a name with special rules. The name of a variable can contain letters, numbers, and the underscore but cannot use spaces or other special symbols.

?> **Tip:** One of the few exceptions to the use of curly brackets for programming-related operations in ink is the use of the `VAR` keyword.

Variables should generally be defined at the beginning of a story before any content to prevent issues where a value may influence possible story output.

## Assigning

Variables must be created with a starting value. This is done using the equal sign, `=`, following the name of the variable and its value in a programming operation named *assignment*:

```ink
VAR name = "Dan"
```

Unlike many other programming languages, ink does not use a semicolon at the end of an assignment. The line ends with the value of a variable.

## Data types

ink supports many types of values including *integers* (whole numbers), *floating point* (decimal), and *strings* (collections of letters, numbers, or special symbols surrounded by quotation marks).

**Note:** Double-quotation marks must be used with string values in ink. Single quotation marks cannot be used.

```ink
VAR exampleInteger = 5
VAR exampleFloatingPoint = 3.14
VAR exampleString = "Hi!"
```

## Conditional text

ink supports the use of comparisons between the value of a variable and some other value. This is known as *conditional text*

To test the value of a variable, the comparison and possible result should be placed within curly brackets, `{}`, with a colon following the comparison and what should run or be shown after the colon inside the curly brackets:

```ink
// Create variables before any other content.
VAR lives = 10
// Conditional text.
// If the value of 'lives' is greater
//  than 5, show some text.
{lives > 5: You are very healthy!}
```

## Showing values

The value of a variable can become part of story output by including the name of a variable within curly brackets by itself:

```ink
VAR name = "Dan"

Hi, my name is {name}!
```

## Updating values

Updating the existing value of a variable can happen at any point in a story after the variable has been created.

To change the value of a variable, use a tilde, `~`, followed by an assignment operation using the name of the variable and a new value.

```ink
VAR name = "Dan"
Hi, my name is {name} and <>
~ name = "Taylor"
my name is {name}.
```

?> **Tip:** The use of the tilde, `~`, is another exception to programming operations using curly brackets.

## Saving alternatives

The result of an alternative can be saved in a variable. However, the variable must exist *before* the use of the alternative:

```ink
VAR day = ""
~ day = "{~Monday|Tuesday|Wednesday|Thursday|Friday}"
Today is {day}.
```

In the previous example, the use of double quotation marks appear around the use of a shuffle. This converts the resulting text into a string value before it is assigned to the variable `day`.
