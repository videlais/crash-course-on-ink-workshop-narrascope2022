# Simple Alternatives

Interactive stories are often composed of both static and dynamic content. So far, we have seen static content in the form of the concepts of lines and comments with using glue to create more complex multi-line output.

Dynamic content takes the form of using *alternatives* with curly brackets, `{}`, around content separated by a bar `|`, between each entry.

?> **Tip** Most programming functionality in ink appears in curly brackets.

## Sequence

A *sequence* is a collection of content where each entry is shown in order until the last:

```ink
{Monday|Tuesday}
```

When run, the next entry in the collection will be selected to generate story content.

## Cycle

A *cycle* is created like a sequence, but starts with an ampersand, `&`, inside the first curly bracket. When run, the collection will move to the next entry and then repeat the "cycle" when it reaches the end:

```ink
{&Monday|Tuesday|Wednesday|Thursday|Friday|Saturday|Sunday}
```

## Shuffle

A *shuffle* appears like a sequence, but uses a tilde, `~`, inside the first curly bracket. A shuffle will select a random entry from its collection each time it is run:

```ink
Today is {~Monday|Tuesday|Wednesday|Thursday|Friday|Saturday|Sunday}
```

## Combining Alternatives

Alternatives can be nested. In order to create more dynamic content, one form of an alternative can be embedded in another.

It is common, for example, to use nested shuffles to have random content generated at different depths or in connection with other, previous selections:

```ink
Today is {~{~rainy |clear-sky }Monday|{~stormy |sunny }Tuesday}.
```

In the previous example, one shuffle is nested inside another. The first shuffle selects between `Monday` or `Tuesday`. Next, the nested shuffle picks between `rainy` and `clear-sky` for `Monday` or `stormy` and `sunny` for `Tuesday`.
