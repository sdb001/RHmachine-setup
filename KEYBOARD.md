# 🛸 RHmachine keyboard guide

For the downloadable **2.1.0-beta.1** terminal app. Press **?** inside the app for help. Uppercase shortcuts mean **Shift + that letter**. Shortcuts depend on the active tab and focused panel; while typing, letters enter text.

## Open a tab

| Key | Tab |
| --- | --- |
| `1` | Radar |
| `L` | Long.xyz |
| `P` | PONS |
| `S` | Split Radar — PONS and Long side by side |
| `R` | Wallet Rotations |
| `2` | Watchlist |
| `3` | Wallets |
| `4` | Positions |
| `5` | Money Flows |
| `6` | AI |
| `7` | Feeds — provider status, errors and coverage |
| `8` | Events |
| `9` | Journal |
| `0` | Settings |

## Navigate and scroll

| Key | Action |
| --- | --- |
| `Tab` / `Shift+Tab` | Next / previous tab; in Split, switch panes |
| `←` / `→` | Previous / next tab, including from Split |
| `↑` / `↓` or `k` / `j` | Move the selection; scroll when reading details or a focused panel |
| `Home` / `End` | First / last row, or beginning / end of the focused text |
| `Page Up` / `Page Down` | Move one page |
| `Enter` | Open the selected row's details |
| `Esc` | Return from details, cancel an edit, or clear search |
| `]` | Switch focus between list and right panel; in Split, switch panes |
| `/` | Search where supported, including coin symbol, contract or name |
| `Enter` while searching | Apply search |
| `Esc` while searching | Cancel and clear search |
| `?` | Open / close help; arrows scroll help |
| `q` or `Ctrl+C` | Quit; `q` is text while typing |

On a Mac keyboard without dedicated navigation keys, try **Fn+←/→** for Home/End and **Fn+↑/↓** for Page Up/Down, depending on your terminal's mappings.

## Coin actions

| Key | Action |
| --- | --- |
| `d` | Open the selected coin's DexScreener page; also works for positions, alerts and events with a contract |
| `i` | Request Hermes analysis of the selected coin or supported wallet row; consumes your configured AI/provider usage |
| `w` or `*` | Add / remove the coin from Watchlist |
| `h` | Hide a Radar coin; restore it when viewing hidden coins |
| `H` | Show hidden Radar coins / return to normal view |
| `f` | In Radar, Long or PONS: cycle all, volume spikes, archived and high-risk views |
| `t` | In Radar views: toggle tracked-source filtering |
| `c` | Track / untrack the selected wallet or source where available |
| `Space` | Open an eligible market candidate as a **paper** position |
| `x` | In Positions: close the selected open **paper** position |

Read-only wallet holdings cannot be sold with `x`. Private wallet/trading extensions are not included in this download; `b` is not a standard beta trading shortcut.

## Split Radar

Press **S**. PONS appears on the left and Long on the right. **Tab**, **Shift+Tab**, or **]** switches the focused pane. Each side remembers its selection and scroll position.

Use **↑/↓**, **Home/End** and **Page Up/Down** within the focused side. **i**, **d**, **w**, **h**, search and filters act on that side. **Enter** opens its report; **Esc** returns. Return from the report before using Tab to switch sides. In a narrow terminal, only the focused pane appears.

## Hermes chat and saved charts

| Key sequence | Action |
| --- | --- |
| `]`, then `a` | Focus the right panel and start a question about the selected coin |
| `Enter` while typing | Send the question |
| `Backspace` / `Esc` | Edit / cancel the question |
| `v` with right panel focused | Switch between report and chat |
| `↑/↓`, Page Up/Down, Home/End | Scroll the focused report or chat independently |
| `o` — lowercase letter O | Open the saved chart image associated with the selected report/reply |

`d` opens DexScreener; `o` opens an existing saved image. Opening the image does not fetch new candles. A report without a saved image cannot provide one through this shortcut. Hermes must be connected for dashboard analysis/chat; configuring another MCP client alone does not connect `i`.

On the **AI tab with the list focused**, `a` cycles **OFF → REVIEW → AUTO** instead of opening chat. REVIEW queues alerts for manual analysis. AUTO can consume AI and research-provider credits; choose it deliberately.

## Wallets, flows and rotations

| View | Key | Action |
| --- | --- | --- |
| Wallets | `f` | Cycle holdings, PnL and movements when those feeds are enabled |
| Wallets | `c` | Bookmark / unbookmark the selected source |
| Money Flows | `f` | Cycle 1h, 6h, 12h and 24h windows |
| Money Flows | `s` | Cycle buying, selling and activity order |
| Money Flows | `t` | Toggle all tracked wallets / cached smart-money and profit labels |
| Rotations | `t` | Toggle clear / ambiguous routes; the time window stays 2h |
| Rotations | `/` | Search source, destination or wallet |
| Rotations | `Enter` | Inspect the underlying transactions |
| Rotations | `d` / `i` | Open the destination chart / request destination analysis with rotation evidence |

Flow windows end at the saved snapshot time. `r` does not force a new flow snapshot.

## Settings and refresh

Press **0**, select a setting with **↑/↓**, then **Enter**. For AI mode and hide-high-risk choices, use **↑/↓** and **Enter** to save. For editable values, type the value and press **Enter**. **Esc** cancels.

| Key | Action |
| --- | --- |
| `r` | Refresh providers |
| `p` | Pause / resume scanner processing; live provider refresh continues |

For API credentials, use the local setup wizard described in [SETUP.md](SETUP.md). Never paste API secrets or private keys into dashboard chat or a public issue.

[Setup instructions](SETUP.md) · [Download the beta](https://github.com/sdb001/RHmachine-beta/releases/tag/v2.1.0-beta.1)
