# Example: *Adventure!*

```ink
// Variables must be created with default values.
VAR race = ""
VAR location = ""
VAR feature = ""
// Set the random location.
~ location = "{~forest|fortress}"
// Set the race.
~ race = "{~humans|mermaids|gnomes|elves}"
// Set the feature.
~ feature = "{~shrine|tower|grotto}"

"Ready for an adventure?" you ask the players sitting before you at the table. 
You consult your notes and begin to read.
"Before you stands a {location} filled with {race}.
Looking closely, you see a {feature}."
```
