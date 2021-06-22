# QMK Keyboard Firmware for HHKB with HASU BT alternative controller

## Layers
BASE, HHKB, MOUSE

### Layer 0 - Base:
```
    /* ,-----------------------------------------------------------.
     * |Esc|  1|  2|  3|  4|  5|  6|  7|  8|  9|  0|  -|  =|  \|  `|
     * |-----------------------------------------------------------|
     * |Tab  |  Q|  W|  E|  R|  T|  Y|  U|  I|  O|  P|  [|  ]|Backs|
     * |-----------------------------------------------------------|
     * |Contro|  A|  S|  D|  F|  G|  H|  J|  K|  L|  ;|  '|Enter   |
     * |-----------------------------------------------------------|
     * |Shift(  |  Z|  X|  C|  V|  B|  N|  M|  ,|  .|  /|Shift)|Fn5|
     * `-----------------------------------------------------------'
     *       |MO1|Alt  |         Space         |MO1  |Gui|
     *       `-------------------------------------------'
     */
```
Default layer, replaced `Shift` with Quantum keys.

### Layer 1 - HHKB: Add media control and dynamic macros.
```
    /* ,-----------------------------------------------------------.
     * |Pwr| F1| F2| F3| F4| F5| F6| F7| F8| F9|F10|F11|F12|Ins|Del|
     * |-----------------------------------------------------------|
     * |Caps |MPv|MPl|MNx|   |   |   |   |Psc|Slk|Pus|Up |   |Backs|
     * |-----------------------------------------------------------|
     * |      |VoD|VoU|Mut|   |   |  *|  /|Hom|PgU|Lef|Rig|Enter   |
     * |-----------------------------------------------------------|
     * |        |DMP|DMP|REC|REC|DRE|  +|  -|End|PgD|Dow|      |   |
     * `-----------------------------------------------------------'
     *       |   |     |                       |     |   |
     *       `-------------------------------------------'
     * REC: Dynamic Record Start / DRE: Dynamic Record End / DMP: Dynamic Macro Play
     */
```
Hold `MO1` to use HHKB layer.\
Start record: `MO1` + `c` or `MO1` + `v`\
End record: `MO1` + `b`\
Play macro: `MO1` + `z` or `MO1` + `x`

### Layer 2 - MOUSE:
```
    /* ,-----------------------------------------------------------.
     * |Esc| F1| F2| F3| F4| F5| F6| F7| F8| F9|F10|F11|F12|Ins|Del|
     * |-----------------------------------------------------------|
     * |Tab  |   |   |   |   |   |MwL|MwU|McU|MwD|MwR|   |   |Backs|
     * |-----------------------------------------------------------|
     * |Contro|  |Acl2|Acl1|Acl0|  |Mb2|McL|McD|McR|Mb1|  |Return  |
     * |-----------------------------------------------------------|
     * |Shift   |   |   |   |   |Mb3|Mb2|Mb1|Mb4|Mb5|   |Shift |   |
     * `-----------------------------------------------------------'
     *      |    |Alt  |           Mb1          |Fn   |Fn |
     *      `--------------------------------------------'
     * Mc: Mouse Cursor / Mb: Mouse Button / Mw: Mouse Wheel
     */
```
Hold `;` to use WASD-style mouse key.\
use `i` `k` `j` `l` as up, down, left, right.\
use `u` `o` to control mouse wheel.
use `s` `d` `f` to control mouse acceleration.

### Known issue
HHKB_RN42_ENABLE rule is not working in keymap folder, set it in keyboard folder or use HHKB_RN42_ENABLE=yes while compiling.\
Console feature can not be disabled while using bluetooth.

### Compile
make hhkb:yimao HHKB_RN42_ENABLE=yes

