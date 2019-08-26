# usbmemory
USB-memory host library for PIC32MX250F128B and PIC32MX270F256B

## How to use
Include .h files and .a file in the project. This library does not contain USB_ApplicationEventHandler() function, which is required for USB-memory host implementation and must be defined in each project. Refer KM-Z80 midi project (usb.c) as an example.

## To compile this library
Use XC32 ver 1.32 for comipling the source code.
Select XC32 archiver but not XC32 liner to make library file (.a file).
Following compiler options are recommended:
	Isolate each function in a section (-ffunction-sections)
	Optimization level 1 (-O1)
	Avoid using global pointer (-G0) (only required for usb_host.c)

## License
Provided with Microchip license. See the comments in each file.