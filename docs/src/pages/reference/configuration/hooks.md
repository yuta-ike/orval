---
id: configuration-hooks
title: Hooks
---

### afterAllFilesWrite

Type: `String` or `String[]` or `Function`.

Runs after orval generates client and writes the generated files to the file system. File paths or
their directory is passed as arguments to the script. You can run configured linter tasks on files
that are generated by orval.

```js
module.exports = {
  petstore: {
    hooks: {
      postWrite: 'prettier --write',
    },
  },
};
```