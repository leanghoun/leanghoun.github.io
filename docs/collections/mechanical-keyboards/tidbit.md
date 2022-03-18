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

### References
* [Product Page](https://nullbits.co/tidbit/)
* [Documentation](https://nullbits.co/start/)
* [SSD1306 OLED Driver for QMK](https://docs.qmk.fm/#/feature_oled_driver)

### Updates
* Looks like `#include "bitc_led.h"` is no longer required. It's been added to the main files.
* OLED lines have changed. Screen rotation is throwing an error. Solved by placing `oled_rotation_t oled_init_user(oled_rotation_t rotation) { return OLED_ROTATION_270; }` within `#ifdef OLED_rotation` and adding `OLED_ENABLE = yes` and `OLED_DRIVER = SSD1306` to *rules.mk*.
* Error compiling from `oled_task_user`. Solved by changing `void oled_task_user(void)` to `bool oled_task_user(void)` and adding `return true;`.
* ~~Looks like Caterina-type devices can't enter DFU from keypress.~~ Adding `BOOTLOADER = caterina` to *rules.mk* fixed it!
