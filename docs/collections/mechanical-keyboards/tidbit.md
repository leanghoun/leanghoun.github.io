---
layout: default
title: Nullbits Tidbit
parent: Mechanical Keyboards
grand_parent: Collections
permalink: /docs/collections/mechanical-keyboards/tidbit/
nav_order: 2
---

# Nullbits Tidbit
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

- TOC
{:toc}

---

![Nullbits Tidbit](../../../../assets/images/nullbits-tidbit.jpg)
*Nullbits Tidbit*
{: .fs-2 .text-grey-dk-000 }

![Nullbits Tidbit OLED](../../../../assets/images/nullbits-tidbit-oled.jpg)
*OLED display*
{: .fs-2 .text-grey-dk-000 }

## References
* [Product Page](https://nullbits.co/tidbit/)
* [Documentation](https://nullbits.co/start/)
* [QMK Documentation](https://docs.qmk.fm/)
  - [Full Keycode List](https://docs.qmk.fm/#/keycodes)
* [SSD1306 OLED Driver for QMK](https://docs.qmk.fm/#/feature_oled_driver)

## Building Hex Files
To build a new hex file:
```
cd Documents/GitHub/qmk_firmware/
make nullbitsco/tidbit:leang
```
The new hex file will be located in Documents/GitHub/qmk_firmware/.

## Updates
* Looks like `#include "bitc_led.h"` is no longer required. It's been added to the main files.
* OLED lines have changed. Screen rotation is throwing an error. Solved by placing `oled_rotation_t oled_init_user(oled_rotation_t rotation) { return OLED_ROTATION_270; }` within `#ifdef OLED_rotation` and adding `OLED_ENABLE = yes` and `OLED_DRIVER = SSD1306` to *rules.mk*.
* Error compiling from `oled_task_user`. Solved by changing `void oled_task_user(void)` to `bool oled_task_user(void)` and adding `return true;`.
* ~~Looks like Caterina-type devices can't enter DFU from keypress.~~ Adding `BOOTLOADER = caterina` to *rules.mk* fixed it!
