# StalzONE
Don’t be too harsh. I’m giving away a ready‑made aim script for Stalz for free. It works both with and without Arduino. I recommend using it with Arduino. I don’t guarantee protection against bans, and the script also needs some improvements. Use it wisely.
README: Aimbot Config & Control
README: Aimbot Config & Control
⚠️ Important Warning
This script is intended exclusively for educational and testing purposes (e.g., studying computer vision, input emulation, and OS interaction).
Using it in online games with anti-cheat systems (EasyAntiCheat, BattlEye, Vanguard, etc.) will result in a game account ban. The author is not responsible for any consequences of its use.

📋 About the Project
Aimbot Config & Control is a dual-mode Python tool for automating cursor aiming. It combines:
------------------------------------------------------------------------------
<img width="736" height="390" alt="221308" src="https://github.com/user-attachments/assets/96e8e6c4-83e7-4080-b7f0-ed4e8daf53cf" />

#Computer Vision (OpenCV): Real-time object detection by color (HSV filtering).
#Screen Capture (MSS): High-performance screenshot of a specific monitor area.
#Two Output Modes:
#Arduino: Transmits cursor offsets to a microcontroller for hardware-based mouse control.
#Maus P (Software): Software emulation of movements and clicks via Windows API.
#Graphical Interface (Tkinter): Parameter configuration, system indicator monitoring, and a built-in terminal for logs.

📦 Installation and Launch (Development Mode .py)
This method is suitable if you plan to edit the code.

Step 1: Install Python
Download and install Python from the official website python.org.
Important: During installation, be sure to check the box "Add Python to PATH".

Step 2: Create a Project Folder
Create an empty folder (e.g., aimbot_project) and place the "aimbot.py" script file inside it.

Step 3: Install Dependencies
Open the command prompt (cmd) in the project folder and run the command:

                                                              🤖 - pip install opencv-python numpy mss pywin32 pyserial keyboard    
Step 4: Launch
Run the script as an administrator:

*Right-click on the aimbot.py file.

*Select "Run as administrator".

*If launched with a simple double-click, 

 ````  "mouse emulation will not work." ````


 🤖 Operation Modes
-----------------------------
Option 1: Arduino Mode (Hardware Output)
Use this if you have an Arduino board (Uno, Nano, etc.) for physical mouse movement.

Required Hardware:

Arduino board.
USB cable.
Arduino sketch (code) that accepts a string like dx dy button and moves the mouse.
Configuration:

1)Connect the Arduino to the PC.

2)Find the COM port number in the "Device Manager" (e.g., COM3).

3)In the program interface, enter this number in the arduino_port field (default is COM6).

4)Enter the baud rate in the baud_rate field (default is 115200).

5)Select the "Arduino" mode in the switch.

6)Start the script. The status "Arduino: Connection Established" will appear in the indicators.

7)Important: If the status shows "Not Connected", check if the port is occupied by another program and verify the port number.

-----------------------------

Option 2: Maus P Mode (Software Output)
Use this if you do not have an Arduino or do not need it. Mouse movements are emulated in software.

Configuration:

1)Select the "Maus P" mode in the switch.

2)Keep other settings (color ranges, capture zone) the same.

3)Start the script.

4)Note: In some games running in "Fullscreen Exclusive" mode, software mouse emulation may be blocked by anti-cheat software or the graphics card driver. It is recommended to run the target game in "Borderless Windowed" mode.

-----------------------------
🛠️ Troubleshooting
Problem	Solution-
Mouse does not move	You launched the script without administrator privileges. Restart with admin rights.-

Arduino does not connect	Check the COM port number in the Device Manager. Ensure the port is not occupied by another program.-

Script does not see the game	The game is running in "Fullscreen Exclusive" mode. Switch the game to "Borderless Windowed".-

Antivirus deletes the file	This is a false positive due to input emulation. Add the project folder to exceptions.-

Error ModuleNotFoundError	Libraries are missing. Run the pip install ... command from Step 3.-

Object is not detected	HSV parameters are incorrect. Try increasing min_area or adjusting color thresholds.-

-----------------------------

"📜 License"

This project is an educational example. The code is provided "as is" without warranty.
