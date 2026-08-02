# Version 0.4

* (schematic) raspberry pi uart route to debug header
* (schematic) change pico's uart to a different uart output
* (schematic) LED way to bright
* removed the HDMI enable.  Were never going to not have it
* the hole near hdmi is has different spacing between apple tv V2,V3
* fix footprint to toss link, 
  * see if the part is different between v2 and v3 
* LED holder for front LED wrong
* (schematic) Fix power input to pi
  * currently i need to set it to 4.7 V to get it to work
  * see if it's the PG pin
* (recheck) Move IR sensor.
  * make sure it works with both V2, V3
* (schematic) HID i2c needs a irq line
* (schematic) Add i2c lines for HID device
  * Add pull up resisters
* (finished) SD card semi boots
  * moved D2 under
  * Compute board doesn't have any resistor on line
  * (future) would be helpful to have uart to see what's going wrong
* (schematic) add i2S lines
  * check to see if the order makes difference in the pio block
    * i don't think these matters because were just receiving data.  Not sending i2s data

# Version 0.3

* Input power is swap "done"
* Also 5 Gnd pins and 3 "3.4" volt pins "done"
* Holes for the TOS link need to be moved up just a little "done" - moved it up 1.2mm
* Don't think i have a "Ethernet magnetic transformers" for ethernet port
  * [site talkd about this](https://hackaday.com/2024/03/07/ethernet-for-hackers-transformers-macs-and-phys/)
  * https://jlcpcb.com/partdetail/PulseElec-H5007NL/C6384935
  * https://ww1.microchip.com/downloads/en/Appnotes/VPPD-01740.pdf
  * Parts really big!!!
  * The old one was just 100 ethernet
  * make sure i have the right pinout for ethernet.
    * Top row is positive
  * I need cap's for the ground
* led's didn't work as intended
  * Makes sense since i thought those pins pushed power.  But they were just pull downs
* Mounting holes for the wire's "ethernet/toslink" are fairly larger then they need to be
* added the magnetic isolater
* change the sd card to be one that's cheap on kicad
* rotate the power input

### Topics of Ethernet and magnetic isolator
* https://www.youtube.com/watch?v=ijQMTl7fUOg
* https://yageogroup.com/browse/products?search=Pulse_Layout-Considerations-v7.pdf
* https://www.ti.com/lit/an/snla387/snla387.pdf?ts=1724108747773&ref_url=https%253A%252F%252Fwww.google.com%252F



## Thoughts
* If i put the pico underneath the raspberry pi some i could put the SD card on the top!  One less thing i would need to solder on