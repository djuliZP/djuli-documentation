# Terminal

Contextual help content for the **bottom terminal panel** of the Djuli web application - a combined notification log and command interface where the user can apply quick transformations to the currently-loaded data lines.

## What the Terminal is

The terminal serves two purposes:

1. **Notifications** - system messages (errors, warnings, info) generated while the app runs.
2. **Commands** - short text commands that act on the data lines in the active report (flip, offset, list current changes, etc.).

Each data line in a report has an `id` shown in the *Files → Processed data table*. Most commands take an `id` argument to target a specific line.

## Documented elements

| Folder | Element |
|---|---|
| [`terminalText/`](./terminalText) | The notification / log area where messages are printed |
| [`textInput/`](./textInput) | The command input box - full list of supported commands |
| [`textEnter/`](./textEnter) | The Enter / submit action for the input box |

## Supported commands (summary)

For full syntax see [`textInput/main.md`](./textInput/main.md).

| Command | Effect |
|---|---|
| `help` | List all available commands |
| `flipx(id)` | Flip the targeted data line on the X axis |
| `flipy(id)` | Flip the targeted data line on the Y axis |
| `offsetx(id, value)` | Apply an offset on the X axis |
| `offsety(id, value)` | Apply an offset on the Y axis |
| `showChanges` | List all transformations applied to the current report |
| `cleanOffset` | Clear offset transformations |
| `cleanFlip` | Clear flip transformations |

## Adding a new entry

1. Create `Terminal/<elementName>/main.md`.
2. Add images / GIFs in the same folder using **relative** paths only.
3. Make sure the matching `setContextualHelp('Terminal/<elementName>')` call exists in `djuli-webapp` - otherwise the panel will never load this content.
