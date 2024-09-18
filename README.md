# QMK for keebio/iris/rev8


## keyboard

https://keeb.io/products/iris-essential-model-2-keyboard

## firmware

use qmk to create a .uf2 file from the json keymap file, then double click the left split keypad, drop the .uf2 file into the USB device called RFI-RFD...wait until it flashes (1-3 seconds)

❯ qmk setup
❯ qmk new-keymap -kb keebio/iris/rev8                                                                                                                                                    ─╯
Ψ Generating a new keymap


Name Your Keymap
Used for maintainer, copyright, etc

Your GitHub Username?  [iancleary]
Ψ Created a new keymap called iancleary in: /home/icleary/qmk_firmware/keyboards/keebio/iris/keymaps/iancleary.
Ψ Compile a firmware with your new keymap by typing: qmk compile -kb keebio/iris/rev8 -km iancleary.                                                                                                                                                    ─╯
❯ qmk compile -kb keebio/iris/rev8 -km iancleary

this uses the file /home/icleary/qmk_firmware/keyboards/keebio/iris/keymaps/iancleary/keymap.json as the source file


use <https://config.qmk.fm/#/keebio/iris/rev8/LAYOUT> to make a new file to/from the json, and then run qmk compile (like above) to make the .uf2 file.

reset mode
copy over to USB
