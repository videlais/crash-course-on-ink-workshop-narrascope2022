# Terms

**Nonlinear storytelling:** Stories become *nonlinear* when its content is accessed in a different order than it was written. ink allows authors to create nonlinear stories by breaking up a story into different parts and accessing them dynamically.

**Knot:** A *knot* is a section of a story defined by the use of at least two equal symbols, `==`, followed by a name on a single line. Knots have special rules for their names: they can contain letters, numbers, and the underscore, but cannot use spaces or other special symbols.

**Stitch:** A *stitch* is a sub-section of a story defined inside of a knot using a single equal sign, `=`. The name of a stitch follows the same rules as knots.

**Divert:** A *divert* moves a story to a knot or stitch. It is created using a minus and greater-than sign, `->`. This "points" to the location in the story to move to next.

**END:** Every story has an end. The keyword `END` is a special knot in every story. It marks the end of a story.

**Choice:** A *choice* uses an asterisk, `*`, or plus sign, `+`, to create an option for a player. Sticky choices use the plus sign, as they are "added back" after a player see it.

**Conditional Choice:** Using curly brackets, `{}`, before the text of a choice, a conditional statement can be used to influence if the choice is available or not based on some comparison.

**Weave:** A collection of one or more choices.

**Gathering Point:** A *gathering point* collapses a weave into one point per level. No matter what choice is selected, the gathering point will always be the result. A gathering point begins with a minus sign, `-`, and extends to the end of a line.

**Selective Output:** The text of a choice can be prevented from becoming part of the output by placing its text inside square brackets, `[]`. This is known as *selective output.*
