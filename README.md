# My Skree keyboard layouts

## Current wired layout and custom keycap design

[Keyboard picture](layouts/vial/layered-draft/keycaps.png) · [Close-up](layouts/vial/layered-draft/final-keycap-closeup.png) · [Quick guide](layouts/vial/layered-draft/quick-guide-phone.png) · [Vial layout](layouts/vial/layered-draft/qwerty-layered-draft.vil) · [82-key specification](layouts/vial/layered-draft/keycap-labels.csv)

Reviewed October 24, 2026 for the wired Skree Redgod 5×7+6: **82 keys, exactly three usable layers: Normal, NAV and SYM.** Vial UID `8490061865922939121`, USB `9953:0002`, 12×7 matrix. The firmware has five slots; slots 3 and 4 are transparent and unreachable.

- Familiar QWERTY letters and number positions, backtick beside 1, and ordinary US Shift symbols. Y is on the right hand.
- Left thumb top row is **Ctrl / Space / Alt**, from the outer edge toward the middle gap. These are immediate dedicated keys, as requested. Exactly two base Shifts: beside A and right of slash. Win is on the right outer thumb, away from the left gaming hand; its former left-thumb position is the inert star key. Caps Lock is on NAV+Esc.
- No mod-taps, layer-taps, tap dances, sticky modifiers or active combos. Normal Ctrl+Z/X/C/V/S/F shortcuts remain ordinary chords. The lightning and star keys are unassigned (`KC_NO`) so their eventual macros do not need new caps.
- Hold the left NAV thumb for navigation and controls; hold the right SYM thumb for programming symbols. Release a layer key to exit that layer. Holding both does not create a utility layer: SYM wins where mapped, then NAV, then Normal. Each releases independently.

### Where the controls are

| Function | Keys |
| --- | --- |
| Escape, Tab, F1–F12 | Direct Normal keys |
| Backspace, Enter, Delete | Direct thumb keys; Backspace is on both hands |
| Print Screen | Direct key before F7 |
| Region screenshot | NAV + PrtSc sends Win+Shift+S |
| Arrows | NAV + I/J/K/L = Up/Left/Down/Right |
| Home / End | NAV + U/O |
| Page Up / Page Down | NAV + P/semicolon |
| Insert / Delete | NAV + Y/H |
| Caps Lock | NAV + Esc |
| Scroll Lock / Pause | NAV + F4/F5 |
| Previous / next tab | NAV + comma/period sends Ctrl+PgUp/PgDn |
| Previous track / play-pause / next track | NAV + F7/F8/F9 |
| Volume down / mute / volume up | NAV + F10/F11/F12; direct Mute also available |
| RGB on-off / dimmer / brighter | NAV + F1/F2/F3 |

The tab pair follows the application’s Ctrl+PgUp/PgDn behavior; it works as adjacent-tab navigation in Chrome and adjacent-editor navigation in VS Code. While NAV is held, A/S/D/F are optional plain Win/Alt/Shift/Ctrl modifiers. For example, NAV+F+J/L moves by words; add D to select. There is no timing-dependent home-row behavior on Normal. A separate numpad, Num Lock, application-menu key and application-specific macros were not added; this design keeps its existing scope.

### Symbols

[SYM map](layouts/vial/layered-draft/sym.png): Q–P follow the number-row order `! @ # $ % ^ & * ( )`. Adjacent home-row pairs are A/S = `[]`, D/F = `()`, K/L = `{}`. J is `=`, G is `+`, H is `-`, N is `/`, M is `_`, V is `|`, B is `~`. Comma/period keep their Normal behavior on SYM. All standard US punctuation remains reachable. The right-thumb hold makes the left-hand bracket pairs convenient; familiar top-row parentheses remain as an alternative.

### Keycap design

![82-key design](layouts/vial/layered-draft/keycaps.png)

- FK shine-through XDA: **78 black standard 1U + 2 black homing 1U (F/J) + 2 white standard 1U (NAV/SYM) = 82 caps**.
- Source Code Pro Semibold: aligned normal legends; usual Shift symbol above it; NAV at bottom-left and SYM at bottom-right. Positions identify layers without repeating their names on every key.
- NAV text is 20% larger than the first artwork revision, and navigation arrows are 60% larger. Lights/Bright use full words; track controls use conventional previous/play-pause/next icons. Minus and underscore use distinct vector bars with approximately 0.4 mm strokes.
- All explicitly assigned layer functions are printed, including Insert, Scroll Lock, Pause, media, RGB and tab shortcuts. Transparent/inherited actions do not add labels. White NAV/SYM caps identify the layer selectors.
- F/J use physical bottom-center homing bars, not engraved fake bars. The artwork reserves that area. Bolt/star icons identify the two spare keys without implying a current action.
- [Individual outlined SVGs](layouts/vial/layered-draft/keycap-artwork/) contain only engraving shapes, with no font installation or decorative cap border required. [Actual-size PDF proof](layouts/vial/layered-draft/actual-size-proof.pdf) and [SVG proof](layouts/vial/layered-draft/keycap-artwork/actual-size-proof.svg) use 14 mm working artboards and a 100 mm scale line. Matrix row/column names match the CSV; the proof sheet is a catalog, not the physical keyboard arrangement.
- [Order specification](layouts/vial/layered-draft/ORDER-SPEC.txt) records cap types, artwork conventions and the remaining production checks. Included [font/license](layouts/vial/layered-draft/fonts/) preserves editable typography.

FK’s live XDA Layout editor was checked on October 24: it exposes a `1u homing` shape and per-selected-key black/white switching. [Editor evidence](layouts/vial/layered-draft/fk-options-verified.png). No front/side printing or separate colored legends are assumed. White-cap legend contrast, exact printable area and final laser alignment must be checked in FK’s production proof; preview colors and homing-bar placement are illustrations.

### Validation and loading

**Offline checks passed:** all 410 populated Vial bindings parse; 82 physical positions match the saved matrix; exactly two Shifts; unchanged QWERTY letters/numbers; 21 ordinary US Shift pairs; core controls and all punctuation; no timing features; independent NAV/SYM release orders; 82 unique artwork files; matching legend data; text bounds and no overlapping labels. The latest refinement changes only two Normal bindings: Win and the inert star key trade thumb positions. NAV and SYM bindings are unchanged.

This revision has **not** been written to or physically tested on the keyboard. Before ordering printed caps, load and use the layout long enough to verify reach, thumb comfort and lighting. Connect the halves as usual and plug the PC cable into the right half’s upper USB port. In Vial, save a backup, confirm the matching device, then **File → Load saved layout** and choose `qwerty-layered-draft.vil`. Loading writes to the keyboard. Verify ordinary typing, Ctrl/Shift/Alt, NAV, SYM, and releasing both layer keys in either order.

### Design references

[QMK layer behavior](https://docs.qmk.fm/feature_layers), [QMK tap-hold behavior](https://docs.qmk.fm/tap_hold), [home-row modifier alternatives](https://precondition.github.io/home-row-mods), [Getreuer’s symbol-layer guide](https://getreuer.info/posts/keyboards/symbol-layer/index.html), [Chrome shortcuts](https://support.google.com/chrome/answer/157179?hl=en), [VS Code editor navigation](https://code.visualstudio.com/docs/editing/getting-started/userinterface), [FK custom editor](https://custom.fkcaps.com/custom/create/keycaps), [Source Code Pro](https://github.com/adobe-fonts/source-code-pro).

The design uses dedicated modifiers and simple momentary layers to suit gaming and learnability. It keeps symbols grouped and paired without claiming a universal optimum for every programming language or hand size.

## Previous wired preview (archived; use the current design above)


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
