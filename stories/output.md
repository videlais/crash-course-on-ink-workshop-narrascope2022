# Creating Output

We write a story in ink by writing a story. The *output* of a story, what is generated for a reader, will appear nearly the same as it does when we write we write it with a few important exceptions.

## Flowing downward

The *flow* of a story is ever downward. For example, starting a story with one sentence will mean the next one appears after the first:

```ink
It goes like this,
the forth, the fifth.
```

This may seem very simple, but understanding the flow of a story is an important aspect of creating with ink.

## From one line to the next

The concepts of *flow* and *lines* are closely connected in ink. The flow of a story moves from one line to the next in order. Each line is considered separate:

```ink
1. Well, people, I've been here before.
2. I know this room and I've walked this floor.
```

We can see this in Inky, as each line has its own line number. This helps us understand, in the case of shorter or longer lines, where one stops and the next begins.

## Reminders and notes

Each comment is its own line. We can use them to break up larger content into smaller parts where we leave notes for ourselves and others to better understand the content:

```ink
// Do we really want to quote song lyrics here?
Well, people, I've been here before.
// What if we re-worded this slightly?
I've walked this floor and seen this room.
```

## Gluing lines

Each line is separate. However, it is possible to merge output using *glue*:

```ink
All of this<>
is one line<>
merged<>
together.
```

In the previous example, the four different lines will appear as one in the output of the story.
