# Zettel ID

A Zettel ID is a [[markdown]] file's filename without the extension. Zettel IDs must be unique across the Zettelkasten.

By default, `neuron new`[^new] will use random alphanumeric IDs of length 8, called a "random ID". But you may use arbitrary text as ID as well, called a "title ID".

## When to use *title IDs*

A title ID is one that uses arbitrary text, typically denoting the title of the note. For example, in the link `[[Some note title]]` (see [[linking]]), "Some note title" is the title ID, corresponding to the note filename `Some note title.md`, that is generated in the [[web]] as the HTML file named `Some_note_title.html`.

Use title IDs when you want truly future-proof[^futureproof] link IDs that work on any text editor. However, note that this comes at the cost that you are willing to rename them (manually or using a script[^rename]) across your Zettelkasten if the title ID of any of your notes changes.

Another advantange of using title IDs is that you do not have to specify an explicit title (eg: `# Foo`) in the Markdown file, as neuron will infer it from the filename.[^titleIdEx]

[^titleIdEx]: See [example](https://github.com/srid/r-ScientificNutrition)

## When to prefer *random IDs*

The advantage to using random IDs (which neuron uses by default) is that you do not have to rename links across your Zettelkasten when changing the title of a note. This makes the links slightly less future-proof, however, because for most convenient editing experience you now have to rely on using a text editor (see [[editor]]) that supports expanding them with the title from the note text.

[^new]: See [[create]]
[^futureproof]: See [[philosophy]]
[^rename]: Use `sed` or [sd](https://github.com/chmln/sd) in a script to rename title IDs across your Zettelkasten. Some text editors, like VSCode, may have built renaming support; see [[editor]].
