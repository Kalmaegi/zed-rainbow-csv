# zed_rainbow_csv

🌈Rainbow CSV - zed extension: Highlight CSV with different rainbow colors to make them more readable

Since at the moment zed only opens up some APIs for tree-sitter, so I wrote a special csv-tree-sitter that (somewhat hardcoded).
looks like this:

light theme:
<img width="1384" alt="image" src="https://github.com/weartist/zed_rainbow_csv/assets/17105034/fd90763e-884d-4e86-b086-d4d53d0e015d">
dark theme:
<img width="1358" alt="image" src="https://github.com/weartist/zed_rainbow_csv/assets/17105034/7a24c202-0b14-4382-97c2-fb710348faea">

for tsv, look like this:
<img width="1356" alt="image" src="https://github.com/weartist/zed-rainbow-csv/assets/17105034/06dded71-1fed-4ca3-be96-094bb220f59c">

## Supported Dialects

| Language Name | Separator | Default Extensions |
|---|---|---|
| `Rainbow CSV (,)` | `,` comma | `.csv` |
| `Rainbow TSV (⭲)` | Tab | `.tsv` |
| `Rainbow CSV (\|)` | `\|` pipe | `.psv` |
| `Rainbow CSV (;)` | `;` semicolon | — |

## Custom File Extensions

You can map any custom file extension to a Rainbow CSV dialect using Zed's `file_types` setting in your `settings.json`.

> **Note:** Extensions like `.csvdb`, `.gamedata`, or `.european.csv` shown below are **user-defined examples**, not standardized formats. Use whatever suffixes fit your project.

```jsonc
// Example: map your custom file extensions to Rainbow CSV dialects
{
  "file_types": {
    "Rainbow CSV (,)": ["csvdb", "gamedata"],
    "Rainbow TSV (⭲)": ["csv"],
    "Rainbow CSV (|)": ["dat"],
    "Rainbow CSV (;)": ["european.csv"]
  }
}
```

Common use cases:

- **Custom suffixes** — associate project-specific files (e.g. `.csvdb`, `.gamedata`) with comma or tab dialects
- **Override defaults** — if your `.csv` files actually use tabs, remap `csv` to `Rainbow TSV (⭲)`
- **Glob patterns** — use full glob paths like `"**/exports/*.txt"` to match by directory structure

## Manual Language Selection

For files that don't match any configured extension, open the command palette (`Ctrl+Shift+P` / `Cmd+Shift+P`) and run **language selector: toggle**, then search for the dialect name (e.g. `Rainbow CSV (,)`).

## Sources of inspiration

https://github.com/mechatroner/vscode_rainbow_csv
