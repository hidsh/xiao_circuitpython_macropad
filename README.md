# xiao_circuitpython_macropad

This is tiny prototype of USB macro pad using [seeduino XIAO](https://wiki.seeedstudio.com/Seeeduino-XIAO/) and [curcuitpython](https://circuitpython.org/).
It is made on a bread board.

It needs download and install `.uf2` from [here](https://circuitpython.org/board/seeeduino_xiao/). 

This repo is based on [CircuitPython Keyboard Emulator](https://learn.adafruit.com/circuitpython-essentials/circuitpython-hid-keyboard-and-mouse#circuitpython-keyboard-emulator-2985260-1) from adafruit.

However it contains only the minimum required lib/py in order to use as HID keyboard because XIAO does not have enough flash.
Plus many lines are commented out in `lib/keycode.py` for the same reason.

# memo

`code.py` has some modifications from the one in the [CircuitPython Keyboard Emulator](https://learn.adafruit.com/circuitpython-essentials/circuitpython-hid-keyboard-and-mouse#circuitpython-keyboard-emulator-2985260-1).

## Corresponding of pin outs and keymap 

```
keypress_pins = [board.D10,          board.D5,           board.D6,               board.D8]

keys_pressed  = [Keycode.LEFT_ARROW, Keycode.SPACEBAR,   Keycode.RIGHT_ARROW,    Keycode.F]
```

## Inverting LED polarity

```
# Turn on the red LED
led.value = False

# Turn off the red LED
led.value = True
```

# tested environment

- circuitpython: [7.0.0](https://circuitpython.org/board/seeeduino_xiao/)
- library: [adafruit-circuitpython-bundle-py-20210930.zip](https://circuitpython.org/libraries)
