* STATUS: Coding has not begun! Just forked recently. Not ready for usage.

Arbl is a no-compromise, high performance, grbl based motion control for 8 axis Robot Arm Control. This version of Arbl runs on an Arduino Mega2560 only.

The controller is written in highly optimized C utilizing every clever feature of the AVR-chips to achieve precise timing and asynchronous operation. It is able to maintain up to 30kHz of stable, jitter free control pulses.

It accepts standards-compliant g-code and has been tested with the output of several CAM tools with no problems. Arcs, circles and helical motion are fully supported, as well as, all other primary g-code commands. Macro functions, variables, and most canned cycles are not supported, but we think GUIs can do a much better job at translating them into straight g-code anyhow.

Arbl includes full acceleration management with look ahead. That means the controller will look up to 24 motions into the future and plan its velocities ahead to deliver smooth acceleration and jerk-free cornering.

* [Licensing](https://github.com/gnea/grbl/wiki/Licensing): Arbl is free software, released under the GPLv3 license.

**COMPLETED**

* Change name from Grbl to Arbl

**NEEDS TESTING**

* Map axis A,B, and C to pins in cpu_map.h
* Limit Mask, Direction Mask, and Step Mask code
* Test code on 3 axis GRBL board to see if XY and Z still works.

**TODOS**

* Add / Init gc_block.values.abc similar to gc_block.values.xyz
* Comment out circular Gcodes, no perpendicular axis XY for those.
* Review Jogging codes for need