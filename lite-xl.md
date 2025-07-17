# Lite XL

## How to test regex patterns for REDOs

1. Run `rescue` in the terminal
2. Paste the regex pattern
3. If it returns strings, add them in the string field of `regex101`'s unit test list
4. Look over the steps
5. Fix the pattern

## Files

?

## Strings

?

## Error Messages

### To write the output of a serialized table to a text file

```lua
io.open("/home/raffaele/log.txt", "wb"):write(common.serialize(templates)):close()
```

### To print the content of a serialized table to `stdout`

```lua
print(common.serialize(templates))
```

### To reveal hidden error messages

Wrap the suspected function call with `print(pcall())`

## Data Storage

- look at the `formatter` plugin
- look at the `linter` plugin
- look at the `lsp` plugin
- look at the `snippets` plugin

## lpm (Lite XL Package Manager)

Example of a branch-specific test bottle command: `lpm --repository https://github.com/lite-xl/lite-xl-plugin-manager.git:3.0 run 3.0-preview`

Install a plugin from a specific branch of a custom repo: `lpm install https://github.com/adamharrison/lite-xl-plugins.git:PR/fix-select-colorscheme select_colorscheme`

