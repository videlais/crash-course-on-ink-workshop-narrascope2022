# Making Choices

Choices are a fundamental part of every interactive story. We often want to present choices to players to allow them to influence what happens next during their narrative experience.

## Choices and weaves

A choice is created in ink using an asterisk, `*`, before a line. This is then presented as an option for a player to pick.

```ink
* Pick me!
* No, pick me!
* No, this one!
```

A collection of choices is named a *weave*. By default, when a player encounters a weave, whatever option they chose becomes permanent for their experience.

Each choice is considered a potentially different branch of the overall story. This allows authors to create a *branching narrative* experience where, depending on the choice, the story branches in different ways.

By default, whatever is placed under a choice within a weave becomes what is shown if the choice is selected:

```ink
An example of a branching narrative!
-> tree

== tree
* Branch A
    This is some content!
    -> END
* Branch B
    This is some content!
    -> END
* Branch C
    This is some content!
    -> END
```

In the previous example, each choice creates a branch with its own content and ending. This can also be nested using multiple choices inside others. In these cases, these sub-choices need one additional asterisk per level of weave:

```ink
* Branch A
    ** Sub-Branch AA
    ** Sub-Branch AB
* Branch B
    ** Sub-Branch BA
    ** Sub-Branch BB
* Branch C
    ** Sub-Branch CA
    ** Sub-Branch CB
```

## Gathering together

Increasing the number of choices and sub-choices can quickly create a large number of branching paths, each requiring more content. To partially solve this issue, ink has the concept of a *gathering point* with the minus sign, `-`.

From the previous example, all of the top-level choices can be *gathered* to the same result:

```ink
* Branch A
    ** Sub-Branch AA
    ** Sub-Branch AB
* Branch B
    ** Sub-Branch BA
    ** Sub-Branch BB
* Branch C
    ** Sub-Branch CA
    ** Sub-Branch CB
- No matter what is selected, players will end up here.
```

Gathering points are a powerful way of providing choices, allowing players to select them, and then collapsing a weave from a more complex branching structure into a simpler one.

## Mixing knots and choices

Encountering a weave a second time using a divert can create problems:

```ink
-> choices

== choices
* One
* Two
* Three
-
-> choices
```

In the previous example, each loop back to the knot would eliminate a choice until the player picked them all, at which point the story would crash end without an explicit divert to `END`.

To help fix this, there is an alternative for default choices named *sticky choices*. These use the plus sign, `+`, as they are "added back" to a weave after use:

```ink
In this example, each choice in the weave is a sticky one.
The player can continue to pick from any of them.
-> choices

== choices
+ One
+ Two
+ Three
-
-> choices
```

## Selective output

By default, the text of each choice becomes part of the output when the player selects it. To prevent this from happening, the text can be placed within square brackets, `[]`. This is known as *selective output.*

```ink
In this example, each choice is using selective output.
-> choices

== choices
+ [One]
+ [Two]
+ [Three]
-
-> choices
```
