## How to Flash with A Hex File

We list the instructions below on how to program (aka "flash") the arduino boards. We assume that you have the arduino IDE already downloaded.

1. Create an empty project in the Arduino IDE. The code can be blank.
2. Plug in the arduino. Click on the right pointing arrow button. This will program the arduino with your empty code.
<img src="https://github.com/TrustworthyComputing/Security_Challenge_2025/blob/main/challenges/hardware_setup/EmptyProject.png" alt="" align="center"  title=""  width="400" height="300">
3. Identify the command used program the board. For Windows, it will look something like this:
`"C:\Users\youDee\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/bin/avrdude" "-CC:\Users\youDee\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/etc/avrdude.conf" -v -V -patmega328p -carduino "-PCOM4" -b115200 -D "-Uflash:w:C:\Users\youDee\AppData\Local\arduino\sketches\E93B8BC6EBE5690A9D5E5D782D485388/sketch_jul3a.ino.hex:i" `
<img src="https://github.com/TrustworthyComputing/Security_Challenge_2025/blob/main/challenges/hardware_setup/DocumentName.png" alt="" align="center"  title=""  width="400" height="300">
4. Close the Arduino IDE. If it is still open, the Arduino IDE hold onto the USB port and will deny your from programming the board.
5. Open up command line or terminal. Edit the command to program the board with the location of your hex file
`"C:\Users\youDee\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/bin/avrdude" "-CC:\Users\youDee\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/etc/avrdude.conf" -v -V -patmega328p -carduino "-PCOM4" -b115200 -D "-Uflash:w:C:\Users\youDee\AppData\Local\arduino\sketches\E93B8BC6EBE5690A9D5E5D782D485388/SpeakerMicTest.hex:i" `
6. If the update is successful, reopen the Arduino IDE. Go to Tools -> Serial Monitor.
7. The Serial Monitor should open at the bottom of the screen. Set the Baud Rate to 115200.
<img src="https://github.com/TrustworthyComputing/Security_Challenge_2025/blob/main/challenges/hardware_setup/SerialMonitor.png" alt="" align="center"  title=""  width="400" height="300">
8. Restart the arduino by unplugging and replugging the device back in. You should see the challenge header and any information on the Serial Monitor. Several challenges will require you to send messages to the Arduino via the Serial Monitor.

Good Luck!! 
