# blockchain/NFTCAM

A scientific camera that signs it's picture metadata with a hash of itself destinated to be embeded in a blockchain / NFT system for (among other things) proof-of-ownership (POW) and proof-of-existence (POE).

Hardware used : ESP32 TTGO Camera Plus

# Install
## using arduino IDE
Install Arduino IDE https://linuxhint.com/install_arduino_ide_debian_10/

Install ESP32 in the Board manager and choose “ESP32 Dev”“ or install manually thanks to (Debian) https://github.com/espressif/arduino-esp32/blob/master/docs/arduino-ide/debian_ubuntu.md

I had this error:

 File "/home/me/Arduino/hardware/espressif/esp32/tools/esptool/esptool.py", line 38, in <module>
    import serial
ImportError: No module named serial

I have fixed this issue with following steps:

    Download the pyserial package from: https://pypi.org/project/pyserial/#files
    tar zxvf pyserial-3.0.tar.gz
    cd pyserial
    sudo python setup.py install

Open the .ino file after

git clone https://github.com/anonette/NonFungibleScience

Compile and Transfer 

## using PlatformIO
```bash
#clone repo and switch to platformio branch
git clone git@github.com:anonette/NonFungibleScience.git  && cd NonFungibleScience && git checkout platformio

#install platformio
curl -fsSL https://raw.githubusercontent.com/platformio/platformio-core-installer/master/get-platformio.py -o get-platformio.py && python get-platformio.py
#you can be also get it as vscode extension https://platformio.org/install/ide?install=vscode

#install dependencies
pio lib install
#build
pio run
#upload
pio run --target upload
```
# More infos

https://wiki.idiot.io/esp32-cam_2

# Thanks

https://www.instructables.com/id/Arduino-Selfie-Camera/

https://github.com/dimhoff/ESP32-CAM_Interval/blob/master/exif.cpp
