# rpi-delcom-legacy
Raspberry Pi Ubuntu Mate 16.04 image for use with old Delcom USB keypads.

[Delcom USB keypads](https://www.delcomproducts.com/productdetails.asp?PartNumber=706502-5M) are perfect for use with owlcms4 .
Except for one issue: Delcom [broke the Linux driver in version 4.8](http://www.delcomproducts.com/webnote.asp?id=3) of the kernel, and Raspberry Stretch / Buster no longer recognizes them as keyboards
This was claimed to be fixed in v4.18 of the kernel, but 4.19 kernels don't recognize the Delcoms either.

Furthermore, the workaround (changing the device ID) only works with Delcom switches newer than firmware 53.

This image is a Ubuntu Mate 16.04 image with an old-enough kernel to support old Delcom switches, but which stil has recent updates for Chromium and TeamViewer.  It has been tweaked to not go to screen saver/sleep.

Notes:
  * When using owlcms4, by default the sounds for the down signal and for the timer warnings (90, 30 and 0 seconds) are produced by the browser.  Under Ubuntu Mate 16.04 for Rasberry Pi, this doesn't work (sounds are late and/or distorted). The issue does not occur on other OS (Raspbian, ChromeOS, etc.) but none of these work with older Delcoms.
    * The work-around is to generate the sounds on the server.  Use the "Prepare Competition/Define Fields of Play" buttons to select an audio output for the main laptop (same as things were in owlcms2)
    * This does imply that you cannot use Delcoms on a Raspberry if the server is running in the cloud. You need another kind of device (Chromebook, Windows).
    * This has only been tested on an RPI 3 -- no idea whether this will work on a RPI 4.
    
    ##Installation
      1. Download [Etcher](https://www.balena.io/etcher/)
      2. Download this image
      3. Write the image to an SD card using Etcher, insert into you Raspberry, reboot.
