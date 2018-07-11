# cloneTX2

**To clone TX1/TX2 and flash:**

1. Read system.img from the gold board filesystem partition with the following command:

For TX2:

`sudo ./flash.sh -r -k APP -G clone.img jetson-tx2 mmcblk0p1`

*This creates a clone.img and clone.img.raw in the <top> directory.*

2. If a new board has been flashed with default release images, use the following commands to flash the file system with the gold board image:

Copy clone.img.raw to the <L4T>/bootloader/system.img directory with the following command:

`sudo cp clone.img.raw bootloader/system.img`

3. Flash the clone image to the APP partition with the following command:

For TX2:

`sudo ./flash.sh -r -k APP jetson-tx2 mmcblk0p1`
