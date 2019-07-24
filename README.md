# rpi-mate-legacy
Raspberry Pi Ubuntu Mate 16.04 image for use with old Delcom USB keypads.

Delcom USB keypads are perfect for use with owlcms4 .
Except for one issue: Delcom broke the Linux driver in version 4.8 of the kernel, and Raspberry Stretch / Buster no longer recognizes them as keyboards
This was claimed to be fixed in v4.18 of the kernel, but 4.19 kernels don't recognize the Delcoms either.

Furthermore, a workaround (changing the device ID) only works with Delcom switches newer than firmware 53.

This image is a Ubuntu Mate 16.04 image with old enough kernel, but which stil has recent updates for Chromium and TeamViewer.
It has been tweaked to not go to screen saver/sleep.
