# cloneTX2

**To clone TX2 and flash:**

1. Read system.img from the gold board filesystem partition with the following command:

`sudo ./flash.sh -r -k APP -G clone.img jetson-tx2 mmcblk0p1`

*This creates a clone.img and clone.img.raw in the <top> directory.*

2. Copy clone.img.raw to the <L4T>/bootloader/system.img directory with the following command:

`sudo cp clone.img.raw bootloader/system.img`

3. If the board has already been flashed with default release images, use the following command to flash the clone image to the APP partition:

`sudo ./flash.sh -r -k APP jetson-tx2 mmcblk0p1`

4. If the board has NOT been flashed with default release images, use the following command:

`sudo ./flash.sh -r jetson-tx2 mmcblk0p1`
