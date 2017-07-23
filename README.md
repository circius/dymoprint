dymoprint-wpmp
=========

A few small adjustments to the dymoprint script for the Dymo PnP to make it compatible with the Dymo Wireless PnP.

Basically working, but multi-line write doesn't seem to work - and the best way to adjust font-size is to directly adjust a variable in the script...

cloned for development from http://sbronner.com/dymoprint/

### For ubuntu based distributions:
(should also work for debian, but not tested yet)
use **udev** and **modeswitch** configurations to work with the LabelManager PNP.
**modeswitch** changes the mode (and USB Id) from mass storage device to printer device.

    sudo cp 91-dymo-labelmanager-pnp.rules /etc/udev/rules.d/
    sudo cp dymo-labelmanager-pnp.conf /etc/usb_modeswitch.d/

and restart services with:

    sudo reload udev

([more info](http://www.draisberghof.de/usb_modeswitch/bb/viewtopic.php?t=947))


### Font management

Fonts are managed via **dymoprint.ini**

You may choose any TTF Font you like

You may edit the file to point to your favorite font.

### Additional libraries used:
*(todo..)*
- PIL/PILLOW
- [pyqrcode](https://github.com/mnooner256/pyqrcode) (used v1.0)
- [pyBarcode](https://bitbucket.org/whitie/python-barcode) (used v0.7)


