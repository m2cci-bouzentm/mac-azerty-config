# macOS Linux-style keyboard setup

Final setup used on Mohamed's MacBook Air with AeroSpace and Karabiner-Elements.

## Modifier layout

### MacBook built-in keyboard

| Physical key | Output | Purpose |
| --- | --- | --- |
| Left Control | Command in normal apps | Linux-style copy/paste shortcuts |
| Left Control | Control in Terminal and iTerm2 | Shell shortcuts and signals |
| Left Option | Control + Command | Dedicated AeroSpace Super key |
| Left Command | Option | Linux Alt position |
| Right-side modifiers | Unchanged | Native macOS behavior |

### External keyboards

- Left Control becomes Command in normal apps.
- Left Control remains Control in Terminal and iTerm2.
- Left Windows/Super emits Control + Command for AeroSpace.
- Alt remains Option.
- The rule targets all non-built-in keyboards and excludes Karabiner's virtual keyboard, so replacement keyboards work automatically.

### Terminal shortcuts

- `Ctrl+C` remains interrupt.
- `Ctrl+Shift+C` copies.
- `Ctrl+Shift+V` pastes.

## AeroSpace

AeroSpace listens for the custom `ctrl-cmd` Super chord. This prevents plain Right Command from triggering window-manager actions.

Common shortcuts:

- `Super+Enter`: open iTerm2
- `Super+H/J/K/L`: focus left/down/up/right
- `Super+Shift+H/J/K/L`: move a window
- `Super+1–0`: switch workspace
- `Super+Shift+1–0`: move a window to a workspace
- `Super+R`: resize mode

AeroSpace and Karabiner start automatically at login.

## French layouts

Enabled input sources:

- `French` — Left Alt/Option + `0` produces `@`
- `French – PC` — Right Alt/AltGr + `0` produces `@`

Use physical `Ctrl+Space` to switch layouts. Karabiner passes this chord through as real Control + Space instead of converting it to Command + Space.

Input sources are global in macOS; they are not selected independently per keyboard.

## Active configuration files

- AeroSpace: `~/.aerospace.toml`
- Karabiner: `~/.config/karabiner/karabiner.json`

Before changing mappings, back up both active configuration files. Restart AeroSpace after changing its bindings and restart the Karabiner services after changing its JSON.
