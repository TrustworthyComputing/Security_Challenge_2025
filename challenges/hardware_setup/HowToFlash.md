## How to Flash with A Hex File

We list the instructions below on how to program (aka "flash") the arduino boards. We assume that you have the arduino IDE already downloaded.

1. Create an empty project in the Arduino IDE. The code can be blank.
2. Plug in the Arduino. Click on the right-pointing arrow button. This will program the Arduino with your empty code.
<img src="https://github.com/TrustworthyComputing/Security_Challenge_2025/blob/main/challenges/hardware_setup/EmptyProject.png" alt="" align="center"  title=""  width="500" height="300">
3. Identify the command used to program the board. It is highlighted in white (unfortunately with white font) in the image below. For Windows, it will look something like this:
   
```
"C:\Users\youDee\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/bin/avrdude" "-CC:\Users\youDee\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/etc/avrdude.conf" -v -V -patmega328p -carduino "-PCOM4" -b115200 -D "-Uflash:w:C:\Users\youDee\AppData\Local\arduino\sketches\E93B8BC6EBE5690A9D5E5D782D485388/sampleProgram.ino.hex:i"
```

<img src="https://github.com/TrustworthyComputing/Security_Challenge_2025/blob/main/challenges/hardware_setup/DocumentName.png" alt="" align="center"  title=""  width="500" height="300">
4. Close the Arduino IDE. If it is still open, the Arduino IDE hold onto the USB port and will deny your from programming the board.
5. Open up the command line or terminal. Edit the command to program, replacing the file location and filename with your hex file.

e.g. `C:\Users\youDee\AppData\Local\arduino\sketches\E93B8BC6EBE5690A9D5E5D782D485388/` changes to `C:\Users\youDee\Downloads\`
`sampleProgram.ino.hex` changes to `SpeakerMicTest.hex`

```
"C:\Users\youDee\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/bin/avrdude" "-CC:\Users\youDee\AppData\Local\Arduino15\packages\arduino\tools\avrdude\6.3.0-arduino17/etc/avrdude.conf" -v -V -patmega328p -carduino "-PCOM4" -b115200 -D "-Uflash:w:C:\Users\youDee\Downloads\SpeakerMicTest.hex:i"
```

6. If the update is successful, reopen the Arduino IDE. Go to Tools -> Serial Monitor.
7. The Serial Monitor should open at the bottom of the screen. Set the Baud Rate to 115200.
<img src="https://github.com/TrustworthyComputing/Security_Challenge_2025/blob/main/challenges/hardware_setup/SerialMonitor.png" alt="" align="center"  title=""  width="500" height="300">
8. Restart the arduino by unplugging and replugging the device back in. You should see the challenge header and any information on the Serial Monitor. Several challenges will require you to send messages to the Arduino via the Serial Monitor.

Good Luck!! 
