# Diverts

Most interactive stories are nonlinear. This means sections of the story are divided up into parts and accessed in different orders. In ink, we can create these types of stories using two connected concepts: *knots* and *diverts*.

## Dividing up a story

Frequently, we want to divide up a story into different parts to help us organize its content. These might be chapters, locations, people, or some other logical division. In ink, these sections are called *knots*.

We can create a knot in ink using two equal sign and a name for the section:

```ink
== chapter1
```

There are special rules for the names of knots. They can contain letters, numbers, and the underscore, but cannot use spaces or other special symbols.

## Moving through a story

We move from one section of a story to another using a *divert*. This "points" to the name of the knot.

```ink
-> chapter1

== chapter1
In the beginning, the story started.
```

## Making an ending

Using diverts and knots introduces a new problem. In a nonlinear story, knowing where a story ends becomes difficult. To help with this issue, ink defines a special knot available in every story: `END`. Every story using knots and diverts must define an end:

```ink
-> chapter1

== chapter1
In the beginning, the story started.
-> END
```

## Knots and stitches

A stitch is a subsection of a knot. Using them, we can divide up a knot into smaller parts to access when needed.

```ink
-> TableOfContents

== TableOfContents

= Chapter1
This is chapter 1.
-> END

= Chapter2
This is chapter 2.
-> END

= Chapter3
This is chapter 3.
-> END
```

The first stitch in a knot is considered the default content. When the story moves to this location, the first stitch's content will always be accessed.

Accessing a stitch within a knot follows a *dot notation*. The name of the knot is first and the stitch second with a period, `.`, between them. In the previous example, the second chapter could be accessed by using the divert target of `TableOfContents.Chapter2`:

```ink
// Jump directly to Chapter 2
-> TableOfContents.Chapter2

== TableOfContents

= Chapter1
This is chapter 1.
-> END

= Chapter2
This is chapter 2.
-> END

= Chapter3
This is chapter 3.
-> END
```
