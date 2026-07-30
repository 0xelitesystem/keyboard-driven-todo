# keyboard-driven-todo

A todo list with vim-style keyboard shortcuts. Single HTML file. No mouse required, no buttons, no dependencies.

**Live demo:** https://0xelitesystem.github.io/keyboard-driven-todo/

## Why

Most todo apps over-engineer interaction: drag handles, multi-select toolbars, settings menus. For a personal todo list, all you need is "add, toggle done, delete, navigate." All of those map cleanly to single keys.

This is the smallest todo I'd actually use.

## Use it

Open `index.html` in any browser, or visit the hosted version at `https://0xelitesystem.github.io/keyboard-driven-todo/` once Pages is enabled.

## Shortcuts

| Key | Action |
|---|---|
| `j` / Down | Next item |
| `k` / Up | Previous item |
| `x` / Space / Enter | Toggle done |
| `i` | Add item (appends) |
| `A` | Add item at top |
| `e` | Edit selected item |
| `dd` | Delete selected item (press d twice) |
| `u` | Undo (50 levels) |
| `gg` | Jump to first |
| `G` | Jump to last |
| `/` | Filter by text |
| `!` then `all` / `done` / `todo` | Switch view |
| `?` | Show help in status bar |
| `Esc` | Clear filter / cancel edit |

## State

Todos live in memory only. Closing or refreshing the tab clears them. This is intentional, see [byok-security-checklist](https://github.com/0xelitesystem/byok-security-checklist) for why we don't write to localStorage by default.

If you fork and want persistence, the relevant function is at the top of the script. Add a `localStorage.setItem` call after every `render()` and read it back on load. Acknowledge the trade-off: any XSS on the page can read your todos.

## Tech

- Single HTML file, ~500 lines
- Vanilla JS, no frameworks, no dependencies
- WCAG AA contrast on both themes
- Light and dark themes with OS preference detection

## What it doesn't do

- Doesn't sync across devices (in-memory only)
- Doesn't have priorities, tags, or due dates (those are different products)
- Doesn't support touch gestures (it's keyboard-driven; tap-to-select still works on mobile)
- Doesn't auto-save anywhere

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. See [LICENSE](LICENSE).

## Related

- [terminal-portfolio](https://github.com/0xelitesystem/terminal-portfolio), interactive terminal portfolio
- [regex-tester-with-explainer](https://github.com/0xelitesystem/regex-tester-with-explainer), regex playground
- [single-file-saas-template](https://github.com/0xelitesystem/single-file-saas-template), ship a SaaS in one HTML file
