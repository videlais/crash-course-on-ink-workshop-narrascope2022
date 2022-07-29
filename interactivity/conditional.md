# Conditional Choices

Programming content often appears in curly brackets in ink. When used with choices, this can be used to make *conditional choices.*

## Optional choices

Existing variables and other values can be compared within curly brackets before choices. If the comparison is false, the choice will not be available in the weave:

```ink
// Create a variable.
VAR health = 10
// Use conditional choices.
// The first choice is available.
// The second one is not based on comparison.
* {health > 5} Continue to fight?
* {health < 4} Take a break
```

In the previous example, only the first choice will be available based on the result of the comparison.

## Testing locations

Every location, knot and stitch, is also a variable in a story. This means it can be tested to see if a player has visited the particular location in a story before.

?> **Tip:** Because knots and stitches are also variables, their names follow the same rules as variables.

If a location has not been visited, it will have the value of `0`. If it has been visited at least once, it will have the value of `1`. In ink, `0` and `1` are also considered `true` and `false` values; `0` represents `false` and `1` `true`.

```ink
-> location
== location
// The following will be true.
{location: You have visited this location!}
-> END
```
