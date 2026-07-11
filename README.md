AutoBell System
Project Description
AutoBell is an automated school bell system integrating an Android app with Arduino hardware. It uses a DS3231 RTC for precision timing and EEPROM for persistent schedule storage. Communication occurs via a high-speed FTDI USB-Serial interface through an OTG connection, ensuring reliability without Wi-Fi. Features include a Material Design UI and a 16x2 LCD for real-time status.
Problem & Solution
Problem: Manual bell ringing in schools and offices is often inconsistent, prone to human error, and requires dedicated personnel to monitor the time constantly. If the person in charge is busy or away, schedules are missed, disrupting the daily routine.
Solution: The AutoBell System is an automated hardware-software solution. It uses an Arduino-based controller with a high-precision Real-Time Clock (RTC) to trigger a bell relay exactly on schedule. The system is managed via a user-friendly Android application that allows for easy schedule configuration, time synchronization, and manual overrides via an FTDI USB-Serial connection.
Setup Instructions
Hardware Setup
1.
Wiring:
◦
Connect the DS3231 RTC to the Arduino (VCC to 5V, GND to GND, SDA to A4, SCL to A5).
◦
Connect the I2C LCD Display to the same I2C pins (SDA/SCL).
◦
Connect the Relay Module signal pin to Digital Pin 7.
◦
Ensure the Arduino is connected via an FTDI USB-Serial interface (built-in or external module).
2.
Power: Power the Arduino via the USB port which will also handle data from the phone.
Software Configuration
1.
Arduino:
◦
Open hardware/AutoBell_System.ino in the Arduino IDE.
◦
Install libraries: RTClib and LiquidCrystal I2C.
◦
Upload the code to your Arduino Nano/Uno.
2.
Android App:
◦
Open the AUTOBELL4 project in Android Studio.
◦
Build and install the app on an Android device with OTG support.
Running the Project
1.
Enable OTG in your Android phone settings.
2.
Connect the phone to the Arduino using a USB OTG cable and the FTDI interface.
3.
Open the AutoBell app and grant USB permissions.
4.
The system will auto-sync the time. Add your schedules in the "Schedules" screen and tap "Save to Hardware."
