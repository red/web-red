---
title: GPIO Port for Raspberry Pi
date: 2019-07-18T20:02:07.000Z
author: Nenad Rakocevic
hero_type: image
hero_src: https://images.pexels.com/photos/993019/pexels-photo-993019.jpeg?auto=compress&cs=tinysrgb&h=650&w=940
category: update
tags:
  - Raspberry Pi
  - GPIO
  - port
  - board
  - hardware
  - hack
---


As part of the R&D work on port! datatype in port-type branch, we have implemented a [GPIO](https://en.wikipedia.org/wiki/General-purpose_input/output) driver for [Raspberry Pi](https://www.raspberrypi.org/) boards, as a `gpio://` scheme (no third-party library needed). This work helped define the low-level API for ports written in purely Red/System or a mix of Red and Red/System.

The Raspberry Pi is a very popular board with millions of units sold, so this is a market where Red could be potentially helpful to developers. We could run Red on such boards for years but did not have proper GPIO support, so this is now fixed!

### The current features supported by the GPIO port are:

- auto-detecting the Raspberry Pi board type
- uses /dev/mem or/dev/gpiomem for direct and fast access.
- reading a GPIO pin state.
- writing to a GPIO pin state.
- hardware PWM output support (on capable pins).
- a simple DSL for sending commands.


### Planned (but not scheduled) future features include:

- generating events when a pin state changes.
- software PWM on all GPIO pins.
- a higher-level reactive object layer for a API-less interface.
- various drivers for common peripherals.  

### The source code for the gpio:// scheme can be found [here](https://github.com/red/red/blob/master/environment/schemes/GPIO.red).  


In the short video below, you can find a little pet project meant for testing some of the features. It implements a simple joypad with 4 directions support, a red LED indicating when the pad is active and a green one for notifying when a level is completed. The game is the [Red port](https://github.com/hyzwhu/redbox) contributed by Huang Yongzhao of [Rebox!](https://www.softinnov.org/rebol/rebox.shtml), my old clone of BoxWorld written in Rebol. In the video below, it is running on a Raspberry Pi 3 using our work-in-progress red/GTK backend for Red (contributed by Rcqls), locally merged with the red/port-type development branch (EDIT: that branch has been merged into master now).

[![GPIO](/images/blog/GPIO_thumbnail.jpg)](https://youtu.be/Gqc1nz61PtU "Click for video")

You can find the breadboard layout below made using [Fritzing](http://fritzing.org/). Sorry for the messy wiring, it is my first try with such kind of tool. If you have the skills to improve it, here is the [sketch file](https://static.red-lang.org/sketches/RPi3-joypad.fzz). The buttons rely on the internal pull-down resistors. Note that in the video, the board is reversed.

![RPi3-jopad](/images/blog/RPi3-joypad_bb.png)

The source code of Redbox has been modified to add GPIO support, you can find the modified code [here](https://gist.github.com/dockimbel/46b358bdda64f60c7f7aaa9e2bc32033). The GPIO-related code is enclosed in a context:

```
joypad: context [
    mapping: [
        16 down  20 up
        17 left  21 right
    ]

    row: [(id) state: #[false] direction: (direction)]
    table: collect [
        foreach [id direction] mapping [keep compose row]
    ]

    pins: extract table length? row
    port: none

    acquire: has [pin][
        port: open gpio://
        foreach pin pins [
            insert port [
                set-mode  pin in
                pull-down pin
            ]
        ]

        insert port [
            set-mode 18 out
            set-mode  4 out
            set 4 on
        ]
    ]

    pressed?: function [][
        foreach pin pins [
            entry: find table pin
            old: entry/state

            insert port [get pin]
            entry/state: make logic! port/data

            ;-- detect 0-to-1 transitions only, to avoid auto-firing
            if all [not old entry/state][return entry/direction]
        ]
        none
    ]

    show-win: does [insert port [set 18 on]]

    release: does [
        insert port [
            set  4 off
            set 18 off
        ]
        close port
    ]
]
```    

### The GPIO port has a simple API:

- opening: `port: open gpio://`
- sending commands: `insert port [...commands...]`
- closing: `close port`


### The sent commands form a small DSL:

- Set the working mode for a given pin

    ```
    set-mode <pin> <mode>

    <pin> : pin number (integer!)
    <mode>: in, out, pwm}
    ```

- Write a value on a pin

    ```
    set <pin> <value>

    <pin>  : pin number (integer!)
    <value>: true, false, on, off, yes, no, 0, 1
    ```
- Read a value from a pin (the returned value is in port/data)

    ```
    get <pin>

    <pin>: pin number (integer!)    
    ```

- Manage pull-up/down resistors

    ```
    pull-off <pin>    ;-- disable any pull previously set
    pull-down <pin>   ;-- activate pull-down on the given pin
    pull-up <pin>     ;-- activate pull-up on the given pin   
    ```

- Write a PWM value on a pin

    ```
    set-pwm <pin> <value>

    <pin>  : pin number (integer!)
    <value>: an integer between 0 and 1024, or a percentage for duty cycle.
    ```

- Fade in/out values on a PWM pin

    ```
    fade <pin> from <start> to <end> <delay>   

    <pin>  : pin number (integer!)
    <start>: starting value (0-1024)
    <end>  : ending value (0-1024)
    <delay>: duration of the whole fading (time!)
    ```

- Wait for a given duration

    ```
    pause <delay>

    <delay>: integer => pause in miliseconds, float => pause in seconds.
    ```

## Important notes

- Only BCM numbering for GPIO pins is supported.

- A word, or path or paren expression containing regular Red code can be used in place of any numeric value.

- A single command block can contain an arbitrary number of commands.

- The `get` command can be used multiple times, a block of corresponding results will then be returned in `port/data`.

- Use `sudo` when running your GPIO code if it involves PWM!

- An example of using `fade` and other commands is available [here](https://github.com/red/red/blob/master/environment/schemes/GPIO.red#L511).

- The PWM range is currently preset to 1024, though, the DSL can be trivially extended to allow a user-provided range value.<br>

### Happy hardware hacking! ;-)