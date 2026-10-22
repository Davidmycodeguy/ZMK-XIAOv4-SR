# My Skree keyboard layouts

## Current wired QMK/Vial layout

[Download the reviewed layout](layouts/vial/qwerty-shift-a.vil) · [Full-size picture](layouts/vial/layout.png) · [Key labels and layer actions](layouts/vial/keycap-labels.csv)

![Reviewed layout, viewed from the typing position](layouts/vial/layout.png)

The October 22, 2026 layout is for the wired Skree Custom Keyboards 5×7+6: 82 physical keys, a 12×7 matrix, five layers, and Vial keyboard UID `8490061865922939121` (USB `9953:0002`).

- Esc is at the top left; F1–F6 follow across the left half.
- Backtick is beside 1. Shift + backtick produces tilde on a US keyboard layout.
- Shift is directly left of A, with the existing Shift beside Z also available.
- Ctrl stays on the left thumb. Mute moves to the left inner bottom key.
- Hold NAV for navigation, SYM for symbols, or both for utilities. Those layers and the thumb mappings retain the earlier wired layout's assignments.

### Load in Vial

Connect the halves as usual and plug the PC cable into the right half's upper USB port. In Vial, select the matching keyboard, save its current layout as a backup, then use **File → Load saved layout** to load `qwerty-shift-a.vil`. Loading a saved layout writes the configuration to the keyboard.

**Status:** the 410 populated layer bindings passed offline Vial keycode validation. This revision has not yet been written to or physically tested on the keyboard. Check typing, modifiers, and both layer keys after loading it.

## Earlier wireless ZMK firmware

The existing `boards/`, `config/`, `build.yaml`, and build workflow describe the older XIAO BLE/ZMK setup. Its [Skree keymap](boards/shields/skreecustom/skreecustom.keymap) remains the reference for that wireless firmware. The current wired layout above is loaded through Vial and does not require rebuilding ZMK.
