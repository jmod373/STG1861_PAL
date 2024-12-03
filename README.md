# STG1861_PAL and PAL1862

The STG1861 is a replacement for the RCA CDP1861 "Pixie" video chip.  The STG1861 uses two 22V10 GALs, a 74HC4040, and a 74HC165 to create a pin compatible replacement for the CDP1861.
This project is an initial proof of concept that builds upon the STG1861 to add colour video.
The project contains a partial implementation of the CDP1862 using a GAL, a number of logic chips and an NTSC/PAL encoder.
This is not a freestanding 1862 replacement as it produces video directly and is dependent on the STG1861_PAL which has signals not available on an original CDP1861.
The PAL1862 can produce a video signal for either PAL or NTSC based on the master crystal which is 2 times the burst frquency. Either 7.15MHz for NTSC or 8.86MHZ for PAL.
My goal was to reproduce the 192x64 video resolution and timing of the CDP1864 for my particular application.
The STG1861 has been modified as STG1861_PAL to match the 1864 timing although NTSC should be possible if the original STG1861 is modified to include Hblank and Vblank signals. I have not tested this as my interest is the PAL functionality.
PAL non-interlaced mode is used and the frame timing is based on 313 lines.
This proof of concept has been tested on the HEC1802 running an ETI660 ROM with 48x64 resolution.
The HEC1802 requires a modification to display colour information correctly with this solution.
The connection from Pin 21 of the CDP1822 and Address Bus 9 must be changed to Address Bus 8. 
The HEC1801 is developed by Costas Skordis at https://github.com/cskordis/HEC1802-Color

