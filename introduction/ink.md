# Working with ink

[ink](https://github.com/inkle/ink), with a lowercase 'i', is a narrative scripting language.

## *Scripting narratives?*

When we use the term *narrative* we mean "what a reader experiences based on text and other content presented to them." Each person comes to a work with various expectations and knowledge. Each experience interacting with a work, be it playing, reading, or some other verb, is slightly different, but they are all *narratives*.

A *scripting language* is a description of a kind of programming language where an author writes code and another program interprets it for a computer to run. When using ink, we write code and a special kind of program called a "runtime" handles the interpretation for us.

Putting the terms together, a "narrative scripting language" is a type of programming language for controlling the content presented to a reader while they are experiencing it, generating a narrative between the user and work.

**In other words, we write words and create code to build stories for others. ink helps us make our stories more dynamic and interactive!**

## A little bit of programming

Writing stories with ink does require using a programming language. However, ink is not scary at all! Learning to use the language is much like learning to use special markup many people use with tools like Discord, Slack, or when using a wiki-based website like Wikipedia.

To write stories in ink, we simply write them. For example, if I wanted to borrow the first line from the book [*Paul Clifford* (1830)](https://en.wikipedia.org/wiki/Paul_Clifford), I would write the following ink code:

```ink
It was a dark and stormy night; 
the rain fell in torrents — except at occasional intervals,
when it was checked by a violent gust of wind which swept up the streets
(for it is in London that our scene lies),
rattling along the housetops, 
and fiercely agitating the scanty flame of the lamps that struggled against the darkness.
```

As we move through this workshop, we will add new special symbols to our ink toolkit to create dynamic and interactive stories.

## *What is ink good at, and what is it bad at?*

ink is best at text-based projects. It is good at dynamic content generation and controlling when different parts of a story are shown to a player.

ink is not good at presentation. The language does not contain any styling functionality. You cannot make text have different colors or be bigger or smaller, for example. ink leaves such functionally up to things it might be working within such as a web browser or game engine.
