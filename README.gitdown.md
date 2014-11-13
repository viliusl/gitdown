## Usage

```js
var gitdown;

// Read the markdown file written using the Gitdown extended markdown.
// File name is not important. "{name}.gitdown.md", "{name}.md" is recommended convention.
gitdown = Gitdown.read('./README.gitdown.md');

// If you have the subject in a string, call the constructor itself:
// gitdown = Gitdown('literal string');

// Output the markdown file.
gitdown.write('./README.md');
```

## Syntax

Gitdown extends markdown syntax using JSON:

```
<<{"gitdown": "method name", "parameter name": "parameter value"}>>
```

JSON strings that are not encapsulated in `<<>>` will remain untouched.

The JSON object must have `gitdown` property that identifies the method. The rest is a regular JSON string, where each property refers to named configuration property of the method you are using.