# T41U5XBB-V3

Repository for an updated version of the T41U5XBB grblHAL Breakout Board

## Aug 25, 2026

Added 3D models for V3.02.

## Aug 24, 2026

Status update. After a hiatus due to daughter's wedding planning and work, I returned to this project. Focused on the same buck converter design for RP23CNC V2.  Ringing problems solved, buck converter is stable and can deliver up to 1A of 5V current.  Applied same design to T41U5XBB V3.  Making a few more changes to the board. Notably, added UART 2 and the ability to alternately use 2.54mm 1x2 pin headers in place of the screw terminals. UART 2 will repurpose the Door and Limit B inputs. Many silk screen changes. Getting close to sending it out for a prototype run.  Will call it V3.02.

## June 17, 2026

Status Update.  Ringing problems with buck converter forced redesign.  Will update here as we progress.

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

