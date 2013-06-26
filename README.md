STM32F3-Mouse
=============

A HID Mouse Project for the STM32F3 Discovery board.

It utilizes the accelorometer for XY movement and the USER button for left clicking.

Features
--------
* XY Movement
* Left Clicking/Dragging
* Only polls when changes are present

Usage
--------
* IDE: Edit with [Atollic TrueSTUDIO for ARM LITE (free)](http://www.atollic.com/index.php/download/truestudio-for-arm)
* Plug in USB cable to USB ST-LINK port on board to program then plug in another USB into the USB USER port (only need USB USER port once done programming)

HID Spec
--------
| Byte  | Bit  | Description                  |
| ----- | ---- | ---------------------------- |
| 0     | 0    | Left Click                   |
| 0     | 1    | Right Click                  |
| 0     | 2    | Middle Click                 |
| 0     | 4-7  | Device-specific              |
| 1     | 0-7  | X displacement               |
| 2     | 0-7  | Y displacement               |
| 3-n   | 0-7  | Device specific (optional)   |
*[Source: (page 61)](http://www.usb.org/developers/devclass_docs/HID1_11.pdf)*
