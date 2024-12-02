# STG1861_PAL

The STG1861 is a replacement for the RCA CDP1861 "Pixie" video chip.  The STG1861 uses two 22V10 GALs, a 74HC4040, and a 74HC165 to create a pin compatible replacement for the CDP1861.
This project is an initial proof of concept that builds upon the STG1861 to recreate the colour video output produced by a CDP1864.
Video output is 192x64 to achieve the video timing of the CDP1864 rather than the 128x64 of the CDP1861.
To achieve this, PAL non-interlaced mode is used and the frame timing is based on 313 lines.
This is not a CDP1864 replacement as it produces the video output only, not the audio portion of the chip.
This proof of concept uses some of the pins of the CDP1862 for the colour portion for testing on the HEC1802.
This solution has been tested on the HEC1802 running an ETI660 ROM with 48x64 resolution.
The HEC1802 requires a modification to display colour information correctly.
The connection from Pin 21 of the CDP1822 and Address Bus 9 must be changed to Address Bus 8. 
