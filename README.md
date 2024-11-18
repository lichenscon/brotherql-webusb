# BrotherQL Label Printer WebUSB Demo

_Check out the [demo on GitHub Pages](https://tylercrumpton.github.io/brotherql-webusb)!_

This little tool is a work-in-progress that will eventually allow you to
print images on a Brother QL-series label printer directly from the
browser, no drivers or installation needed! Just plug your printer's USB
cable into your computer, select an image, and click the "Print Label"
button to get started.


## How It Works
The page uses the [WebUSB API](https://developer.mozilla.org/en-US/docs/Web/API/WebUSB_API) 
to communicate directly to your Brother label printer over USB. It
manually converts the selected image to monochrome and generates the
necessary raster data to print it on the label printer. The printer
commands are sent as a series of bytes to the printer using the WebUSB
API.


## Prototyping Note
This is a work-in-progress protoype and is hardcoded to work with a 
Brother QL-700 printer and a 62mm x 29mm die-cut label roll. Most 
of the guts are ready to be expanded to other printers, labels, and 
features, but I've not gotten there yet.


## Credits
This work is heavily inspired by the [brother_ql](https://github.com/pklaus/brother_ql)
Python library by Philipp Klaus that uses PyUSB to send commands to
Brother QL-series label printers.
