# QMK for keebio/iris/rev8


## keyboard

https://keeb.io/products/iris-essential-model-2-keyboard

## keymap

[picture of printed keymap from config.qmk.fm website](./keymap.png)

## firmware

setup qmk (once per machine or to get latest qmk software)
use config.qmk.fm to create json keymap file
use qmk to create a .uf2 file from the json keymap file
enter bootloader mode on keyboard by double clicking left side reset buttom (hole in bottom of case with button)
  left side is main controller in default QMK setups
drop the .uf2 file into the USB device called RFI-RFD...wait until it flashes (1-3 seconds). Hooray.

### qmk configurator

load json file from this repo to start (or else you start from the default for your keyboard!)
<https://config.qmk.fm/#/keebio/iris/rev8/LAYOUT>
download json file to disk

~
### qmk setup

Setup enables us to compile json to uf2 files used for flashing

nix-shell -p qmk

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

### Enter bootloader mode on keyboard to flash/load uf2 file onto keyboard

<https://docs.keeb.io/flashing-firmware#rp2040-board-uf2-bootloader>

- Enter bootloader mode (use one of the following methods):
  - Double-tap the Reset button
  - Hold the Reset button for at least 1 second and then let go
- Wait for OS to detect the board in bootloader mode
  - It will show up as a USB mass-storage device named RPI-RP2
- Copy the .uf2 file to the RPI-RP2 USB drive







use <https://config.qmk.fm/#/keebio/iris/rev8/LAYOUT> to make a new file to/from the json, and then run qmk compile (like above) to make the .uf2 file.

reset mode
copy over to USB
