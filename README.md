# My Skree keyboard layouts

## Current wired QMK/Vial layer draft

[Download the layered draft](layouts/vial/layered-draft/qwerty-layered-draft.vil) · [Base layout](layouts/vial/layered-draft/base.png) · [Custom cap legends](layouts/vial/layered-draft/keycaps.png) · [All 82 labels](layouts/vial/layered-draft/keycap-labels.csv)

The October 22, 2026 draft keeps the familiar QWERTY letter and number positions and adds readable NAV, SYM, and utility functions. It targets the wired Skree 5×7+6 with 82 physical keys, a 12×7 matrix, Vial UID `8490061865922939121`, and USB `9953:0002`.

- Exactly two Shifts: beside A and on the right thumb. The freed positions are Caps beside Z, Win on the left thumb, and Ctrl on the right pinky. Left-thumb Ctrl remains available.
- [NAV](layouts/vial/layered-draft/nav.png): hold the left NAV thumb key. I/J/K/L are Up/Left/Down/Right; U/O are Home/End. Right Ctrl allows word movement while NAV is held; add the left Shift to select words. The left hand has tab, history, find, and editing shortcuts. Right-thumb Backspace/Delete delete words.
- [SYM](layouts/vial/layered-draft/sym.png): hold the right SYM thumb key for punctuation, brackets, braces, and parentheses without Shift. The base backtick stays beside 1; Shift produces tilde with a US keyboard layout.
- [Utilities](layouts/vial/layered-draft/util.png): hold both thumb keys in either order. F1–F6 control lighting; F7–F12 control media and volume. Mute becomes Hue+ and PrtSc becomes Windows region screenshot (`Win+Shift+S`). Other keys retain base actions regardless of thumb press order.
- Cap draft: large base legend, NAV at the lower left, SYM at the lower right. Utility labels sit on the function row, PrtSc, and Mute. The image colors explain the layers; the intended printed legends can all be white. The fifth firmware layer is unused.

**Status:** all 410 populated bindings passed offline Vial parsing. Checks also cover two Shifts, unchanged alphanumerics, standard US punctuation, usable modifiers, and both thumb press/release orders. This draft has not been written to or physically tested on the keyboard. Cap font, spacing, and lighting still need the manufacturer's final proof.

To load, connect the halves as usual and plug the PC cable into the right half's upper USB port. Save a backup in Vial, confirm the matching keyboard, then choose **File → Load saved layout** and select `layered-draft/qwerty-layered-draft.vil`. Loading writes the configuration to the keyboard. Check typing, modifiers, navigation, symbols, and both layer keys on the hardware.

![Draft custom cap legends, viewed from the typing position](layouts/vial/layered-draft/keycaps.png)

## Previous wired preview

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
