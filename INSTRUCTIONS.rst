How to PineTime 
==================================

Connecting to Pinetime on a Raspberry Pi
----------------------------------------------------
Start the watch normally (not a DFU mode)

In a command line start 'bluetoothctl scan on' to find the MAC
adress of the watch. It should look something like this: 

Device EC:X:X:X:X:X PineTime

Connect to the watch in the command line tap: 
'bluetoothctl connect EC:90:F3:05:E6:27'

Now you can use the wasptool to send commands to the watch and fetch
the data from it 

To check if it worked, try this command from the wasp-os directory.
It should reset the time on the watch to current time. 

~/wasp-os $ ./tools/wasptool --rtc