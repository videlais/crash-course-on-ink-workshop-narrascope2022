# Story Terms

**Project / Story**: When using the Inky editor, combining one or more files into a single work creates a *project*. At the same time, when the content is run, the term *story* is used. Generally, when discussing files, the better term is "project" and when describing its possible output or what a reader might see, the better term is "story."

**Flow**: Content runs downward. When a story is run, the beginning of the story appears at the top and the end of the story is at the bottom. The *flow* of the story follows the path from top to bottom, unless redirected by the author.

**Line**: The smallest unit of content in a project is a *line*. This is any content starting on a new line and continuing until the next new line.

**Glue:** Using less-than and greater-than symbols together, `<>`, creates *glue*. This appends the content following with the line appearing before it. This allows authors to merge content together.

**Comment:** A *comment* is any content appearing in a project as notes or instructions for authors. A comment is not story content and will not appear to a reader. Comment begins with two slashes, `//`, and ends with a new line.

**Alternatives:** An *alternative* in ink describes any use of programming to generate dynamic story output. These take the form of *sequences*, where content uses each entry in the collection until the end and stops at the last, *cycles*, where the the collection repeats, and *shuffles*, random entries from the collection are selected each time. Alternatives are defined by a collection of content surrounded by curly brackets, `{}`, where each entry is separated by a bar, `|`.

**Variables:** Values can be tracked using *variables* in ink. They must first be created using the keyword `VAR` and a name following the rules of letters, numbers, and the underscore, but cannot use spaces or other special symbols. Once created, its value can be changed through the story and used to influence content output.
