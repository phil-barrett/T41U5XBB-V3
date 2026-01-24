# T41U5XBB-V3

Repository for an updated version of the T41U5XBB grblHAL Breakout Board

## Jan 24, 2026
Started working on manual update. Borrowing a lot from the RP23CNC manual.
Uploaded V3.00 schematic and V3.00 images.

## Jan 22, 2026
Beta boards mailed.

## Jan 16, 2026
Received first board from fab.  Testing - appears to work correctly on both 12V and 24V. Testing continuing.  Wiil report any issues found.

Evaluated and characterized buck converter.  At 12V verified heat rise 40C over ambient at 1A.  At 24V, 35C at 500 mA. ripple within expectations. Tested 24 hr loads at those draws. No problems found. Pretty happy with the power section so far.

Several issues found:
- Teensy Vin jumper awkwardly placed
- With Vin jumper close, 5V from USB back feeds the buck converter IC.  No harm but looks ugly as it lights the 12/24 LED.  For V3.01, moved to a 2 way jumper for 5V SRC, similar to RP23CNC power scehme. No back feeding the buck IC.
- Wrong schmitt trigger IC for UART 1 header's EStop pin.  Fixed in V3.01.


