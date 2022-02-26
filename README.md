# tailwind-vscode-bug

This repo is a minimal reproduction of the tailwind vscode extension bug where multiple matches to the `classRegex` setting does not give intellisense or autocompletion.

https://github.com/tailwindlabs/tailwindcss-intellisense/issues/499

## Example

Using the following `classRegex` tailwind vscode extension setting:

```json
{
  "tailwindCSS.experimental.classRegex": [["/\\*tw\\*/ ([^;]*);", "'([^']*)'"]]
}
```

You can open [`src/App.tsx:7-13`](https://github.com/benatshippabo/tailwind-vscode-bug/blob/main/src/App.tsx#L7-L13) and see that we get tailwind intellisense for `styles` but not for `styles2`.

## Context

https://github.com/tailwindlabs/tailwindcss/issues/7553#issuecomment-735915659
https://github.com/tailwindlabs/tailwindcss/issues/7553#issuecomment-917271069
