# Agent Instructions for ZMK Keymap

## Keymap Philosophy

This keymap is optimized for a **heavy Vim user** who is **not a fast typer**.

### Home Row Mods Layout
- **Left hand**: GUI, ALT, SHIFT, CTRL (pinky → index)
  - A = GUI, S = ALT, D = SHIFT, F = CTRL
- **Right hand**: CTRL, SHIFT, ALT, GUI (index → pinky)
  - J = CTRL, K = SHIFT, L = ALT, ; = GUI

**Why CTRL on index fingers**: Vim uses CTRL constantly (Ctrl+D/U/F/B/W/O/I, etc.). Having CTRL on the strongest fingers makes Vim navigation much more comfortable.

### Timing Settings
All home row mod behaviors use **forgiving timing** to prevent accidental modifier activation:
- `tapping-term-ms: 450` - Requires ~half second hold before registering as modifier
- `require-prior-idle-ms: 200` - Requires idle time before hold-tap activates
- `quick-tap-ms: 200` - Window for quick repeated taps

**Do not modify these timing parameters without explicit user request.**

## Layer Structure

### Layer 0: Base QWERTY
- Standard QWERTY layout with home row mods
- Thumb keys: GUI/ESC, Layer 1 (hold DEL), BSPC, SPACE, Layer 2 (hold ENTER), ALT

### Layer 1: Numbers and Symbols
- Top row: Shifted symbols (!, @, #, $, %, ^, &, *, (, ))
- Home row: Numbers 1-5 with home row mods, punctuation with home row mods on right
- Bottom row: Numbers 6-0, shifted punctuation

### Layer 2: Function Keys and Navigation
- Top row: F1-F12
- Home row: Modifier keys (left), arrow keys with home row mods (right)
- Bottom row: Sticky layer 3 key, Page navigation

### Layer 3: Bluetooth Controls
- Bottom row: BT_CLR, BT_SEL 0-4
- Accessed via sticky layer (&sl 3) from Layer 2

## Editing Rules

### Critical Requirements
1. **Always align columns across all 4 layers** - Each column position must line up vertically
2. **Preserve home row mod structure** - Don't change the modifier order (GUI, ALT, SHIFT, CTRL)
3. **Don't modify timing parameters** without explicit request
4. **Maintain Vim-optimized layout** - CTRL must stay on index fingers (F/J)

### Formatting Standards
- Use consistent spacing for readability
- Keep bindings aligned in neat columns
- Indent properly within layer definitions

## Common Modifications

### Adding New Keys
- Maintain column alignment across all layers
- Consider if home row mods are appropriate for the position
- Update this file if adding new layers or significant functionality

### Changing Modifiers
- Remember the user is a Vim user - CTRL placement is critical
- Consider typing speed when adjusting timing parameters
- Test changes don't break the forgiving timing for slower typing

## References
- [ZMK Documentation](https://zmk.dev/)
- [Home Row Mods Guide](https://precondition.github.io/home-row-mods)
- [Corne Keyboard Info](https://github.com/foostan/crkbd)
