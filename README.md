

Uses the ZSA fork of QMK:

https://github.com/zsa/qmk_firmware

## Setup

Use the firmware23 branch of zsa

```sh
qmk setup zsa/qmk_firmware -b firmware24
qmk config user.keyboard=zsa/voyager
qmk config user.keymap=cor
```

QMK firmware will now be setup in `~/qmk_firmware/keyboards/zsa/voyager/keymaps/cor`.

Then, remove the default config and link it to this repo's keymap:

```
rm -rf /Users/cor/qmk_firmware/keyboards/zsa/voyager/keymaps/cor
ln -s /Users/cor/dev/voyager-helix-qmk/keymap /Users/cor/qmk_firmware/keyboards/zsa/voyager/keymaps/cor
```

## Compile

```sh
qmk compile
```


## Flash

```sh
qmk flash
```


