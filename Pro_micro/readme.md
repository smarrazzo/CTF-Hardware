# Flash CTF on atmege32U4 (Pro-micro or USBKEY)

## Windows 

First put arduino in flash mode :
`mode.com COM11: baud=1200 dtr=ON  DATA=8`

Then Flash the firmware (Serial port num +1) 
`avrdude "-Cavrdude.conf" -v -V -patmega32u4 -cavr109 "-PCOM12" -b57600 -D "-Uflash:w:CTF_Leonardo.hex:i"`


## Linux 

First put arduino in flash mode :
`python3 reset.py /dev/ttyACM0`

Then Flash the firmware (Serial port num +1) 
`avrdude "-Cavrdude.conf" -v -V -patmega32u4 -cavr109 "-P/dev/ttyACM1" -b57600 -D "-Uflash:w:CTF_Leonardo.hex:i"`
