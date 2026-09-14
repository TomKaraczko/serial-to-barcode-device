# serial-to-barcode-device
Add-on device for package scales with rs-232: display the weight of packages as scanable barcode for easy handling. 
Automated Scale Interface & E-Paper Barcode Display

This custom embedded hardware solution interfaces Adam Equipment CPWplus scales with a Raspberry Pi to automate local barcode generation. The system reads incoming data via a serial connection, dynamically processes the values, and renders the resulting barcodes on a low-power E-Paper screen for high-contrast, persistent visibility.

Hardware Architecture

    Core Controller: Raspberry Pi Zero WH (Prototype: Raspberry Pi 3b) 

    Visual Output: Waveshare 2.13-inch E-Paper HAT Display

    Input Source: Adam Equipment CPWplus scale

    Data Link: RS-232 serial interface bridging the scale and the Raspberry Pi

Software Stack

    Language: Python

    Display Integration: epd2in13_V4 driver library for screen refresh and graphic rendering

    Barcode Generation: Zint Barcode Generator to encode the parsed serial payload into robust, machine-readable barcodes
    
Core Workflow

    Data Acquisition: The system polls the scale over the RS-232 interface to retrieve real-time measurements.

    Processing: A Python script parses the serial payload and triggers Zint to dynamically generate the corresponding barcode image.

    Rendering: The E-Paper display refreshes to show the new barcode, holding the image indefinitely without requiring continuous power.

    No additional devices: this add-on-device runs without periphals or regular monitor. plug-n-display! 

Releases

    I will release the python script as such + the full funtioning raspian-32-bit-image incl autostart-function, script and drivers.

    (A connection to the world wide web will not be possible with this image, since the image is stripped off all network adapter for faster boot and less security concerns.)
# serial-to-barcode-device
Add-on device for package scales with rs-232: display the weight of packages as scanable barcode for easy handling. 
Automated Scale Interface & E-Paper Barcode Display

This custom embedded hardware solution interfaces Adam Equipment CPWplus scales with a Raspberry Pi to automate local barcode generation. The system reads incoming data via a serial connection, dynamically processes the values, and renders the resulting barcodes on a low-power E-Paper screen for high-contrast, persistent visibility.

Hardware Architecture

    Core Controller: Raspberry Pi Zero WH (Prototype: Raspberry Pi 3b) 

    Visual Output: Waveshare 2.13-inch E-Paper HAT Display

    Input Source: Adam Equipment CPWplus scale

    Data Link: RS-232 serial interface bridging the scale and the Raspberry Pi

Software Stack

    Language: Python

    Display Integration: epd2in13_V4 driver library for screen refresh and graphic rendering

    Barcode Generation: Zint Barcode Generator to encode the parsed serial payload into robust, machine-readable barcodes
    
Core Workflow

    Data Acquisition: The system polls the scale over the RS-232 interface to retrieve real-time measurements.

    Processing: A Python script parses the serial payload and triggers Zint to dynamically generate the corresponding barcode image.

    Rendering: The E-Paper display refreshes to show the new barcode, holding the image indefinitely without requiring continuous power.

    No additional devices: this add-on-device runs without periphals or regular monitor. plug-n-display! 

Releases

    I will release the python script as such + the full funtioning raspian-32-bit-image incl autostart-function, script and drivers.

    (A connection to the world wide web will not be possible with this image, since the image is stripped off all network adapter for faster boot and less security concerns.)
