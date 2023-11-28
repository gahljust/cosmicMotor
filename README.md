# Cosmic Ray Stand Motor GUI

This project provides a Graphical User Interface (GUI) for controlling a motor. The GUI is written in C using the GTK+3 library.

## Required Packages

To run this program on a Raspberry Pi, you will need the following packages:

1. **gcc**: the GNU Compiler Collection, used to compile C programs.
2. **libgtk-3-dev**: GTK+3 development files, used to compile programs that use GTK+3.
3. **pkg-config**: helper tool used when compiling applications and libraries.

## Installation

To install these packages on a Raspberry Pi running a Debian-based distribution, such as Raspberry Pi OS, you can use the following commands:

```bash
sudo apt update
sudo apt install gcc libgtk-3-dev pkg-config
```

## Compiling the Program
After you have installed the required packages, you can compile the program using gcc:

```bash
gcc `pkg-config --cflags gtk+-3.0` -o cosmicMotor cosmic_motor.c `pkg-config --libs gtk+-3.0`
```
This command tells gcc to compile the file motor_gui.c and link it with the libraries used by GTK+3, creating an executable file called motor_gui.

## Running the Program
After compiling the program, you can run it with the following command:

```bash
./cosmicMotor
```

Instructional for Mac Users
Follow the steps below to run the program on MacOS:

# Step 1: Install Homebrew
Homebrew is a package manager for macOS that simplifies the installation of software. Open your Terminal and install Homebrew by entering:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
## Step 2: Install GTK+ and pkg-config
You will need the GTK+ library to build the GUI and pkg-config to configure compiler and linker flags. Install them using Homebrew by entering:

```bash
brew install gtk+3
brew install pkg-config
```

## Step 3: Install GCC Compiler
Install the GCC compiler using Homebrew by entering:


```bash
brew install gcc
```

## Step 4: Clone the Repository

## Step 5: Compile the Program
Navigate to the repository directory and compile the source code. Replace <source_file> with the name of your C file:

```bash
gcc `pkg-config --cflags gtk+-3.0` -o cosmicMotor cosmic_motor.c `pkg-config --libs gtk+-3.0`
```

## Step 6: Run the Program

```bash
./cosmicMotor
```

The GUI of the program should now appear on your screen.

Note: The steps above assume that you're using a bash or zsh shell. If you're using a different shell, you may need to adjust some of the commands.

Also, please ensure that the USB device path (/dev/tty.usbserial-A601VOHX) is correct for your system. In MacOS, it is common for the path to be something like /dev/tty.usbmodemXXXX. The exact path can be found from the command `ls /dev/`.

You can check this on a raspberry pi by typing `ls /dev/` while the motor is unplugged, then plugging the motor in and typing `ls /dev/` again and looking at the difference.

## Usage

### Main Functions
### Start Limit Switch
### Button Label: "Start Limit Switch"
* Functionality: Initiates a command to set the start limit of the motor.
End Limit Switch
Button Label: "End Limit Switch"
Functionality: Sends a command to set the end limit of the motor.
Set Position to Zero
Button Label: "Set Position to Zero"
Functionality: Resets the motor's position to zero.
Move Up (Y) / Move Down (Y)
Button Labels: "Move Up (Y)" and "Move Down (Y)"
Functionality: Moves the motor a specific distance in the Y-axis, either up or down, based on the value entered in the distance entry field.
Move Left (X) / Move Right (X)
Button Labels: "Move Left (X)" and "Move Right (X)"
Functionality: Moves the motor a specific distance in the X-axis, either left or right, as per the distance entry.
Get Position
Button Label: "Get Position"
Functionality: Retrieves the current position of the motor and displays it in millimeters.
Clear
Button Label: "Clear"
Functionality: Clears any current operations or commands sent to the motor.
Kill Op.
Button Label: "Kill Op."
Functionality: Immediately stops any ongoing operation of the motor.
Status
Button Label: "Status"
Functionality: Checks and displays the current status of the motor (Running, Busy, or in Jog mode).
Offline
Button Label: "Offline"
Functionality: Sends a command to take the motor offline.
Additional Features
Distance Entry
Widget: Entry field
Purpose: Allows the user to input the distance for motor movement commands.
Position Display
Widget: Label
Purpose: Displays the current position of the motor in millimeters.
Motor Status Display
Widget: Label
Purpose: Shows the current status of the motor.
Installation and Setup
(Provide instructions on how to install and set up the application, including any dependencies or prerequisites.)




