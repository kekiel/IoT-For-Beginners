# Raspberry Pi

The [Raspberry Pi](https://raspberrypi.org) is a single-board computer. You can add sensors and actuators using a wide range of devices and ecosystems, and for these lessons using a hardware ecosystem called [Grove](https://www.seeedstudio.com/category/Grove-c-1003.html). You will code your Pi and access the Grove sensors using Python.

![A Raspberry Pi 4](../../../images/raspberry-pi-4.jpg)

## Setup

If you are using a Raspberry Pi as your IoT hardware, you have two choices - you can work through all these lessons and code directly on the Pi, or you can connect remotely to a 'headless' Pi and code from your computer.

Before you begin, you also need to connect the Grove Base Hat to your Pi.

### Task - setup

Install the Grove base hat on your Pi and configure the Pi

1. Connect the Grove base hat to your Pi. The socket on the hat fits over all of the GPIO pins on the Pi, sliding all the way down the pins to sit firmly on the base. It sits over the Pi, covering it.

    ![Fitting the grove hat](../../../images/pi-grove-hat-fitting.gif)

1. Decide how you want to program your Pi, and head to the relevant section below:

    * [Work directly on your Pi](#work-directly-on-your-pi)
    * [Remote access to code the Pi](#remote-access-to-code-the-pi)

### Work directly on your Pi

If you want to work directly on your Pi, you can use the desktop version of Raspberry Pi OS and install all the tools you need.

#### VNC Remote access via MobaXterm

First, make sure you enable VNC using sudo raspi-config, going to interfacing options, and then for VNC select yes. Then follow the instructions below.

- click the Vnc icon in the top bar, open the hamburger menu, and select "Options..."
- Under the "Security" tab, for "Authentication" choose the "VNC password" option
- Under "Users and Permissions" tab, select "Standard User" and click "Password..." to set your VNC password
- (you might need to reboot)

#### Task - work directly on your Pi

Set up your Pi for development.

1. Follow the instructions in the [Raspberry Pi setup guide](https://projects.raspberrypi.org/en/projects/raspberry-pi-setting-up) to set up your Pi, connect it to a keyboard/mouse/monitor, connect it to your WiFi or ethernet network, and update the software. The OS you want to install is **Raspberry Pi OS (32 bit)**, it is marked as the recommended OS when using the Raspberry Pi Imager to image your SD card.

To program the Pi using the Grove sensors and actuators, you will need to install an editor to allow you to write the device code, and various libraries and tools that interact with the Grove hardware.

1. Once your Pi has rebooted, launch the Terminal by clicking the **Terminal** icon on the top menu bar, or choose *Menu -> Accessories -> Terminal*

1. Run the following command to ensure the OS and installed software is up to date:

    ```sh
    sudo apt update && sudo apt full-upgrade --yes
    ```

1. Run the following command to install all the needed libraries for the Grove hardware:

    ```sh
    curl -sL https://github.com/Seeed-Studio/grove.py/raw/master/install.sh | sudo bash -s -
    ```

    One of the powerful features of Python is the ability to install [Pip packages](https://pypi.org) - these are packages of code written by other people and published to the Internet. You can install a Pip package onto your computer with one command, then use that package in your code. This Grove install script will install the Pip packages you will use to work with the Grove hardware from Python.
    
_Due to chip shortage, we have replaced STM32 with MM32 in the latest version of the product, and the I2C address of the corresponding product has been changed from 0x04 to 0x08 in the old version, please change the I2C address in adc.py from 0x04 to 0x08 when using the library file provided by seed for development._

    sudo nano /usr/local/lib/python3.7/dist-packages/grove/adc.py
    
'RPI_HAT_PID = 0x0008' => 'RPI_HAT_PID = 0x0004'

1. Reboot the Pi either using the menu or running the following command in the Terminal:

    ```sh
    sudo reboot
    ```

1. Once the Pi has rebooted, relaunch the Terminal and run the following command to install [Visual Studio Code (VS Code)](https://code.visualstudio.com?WT.mc_id=academic-17441-jabenn) - this is the editor you will be using to write your device code in Python.

    ```sh
    sudo apt install code
    ```

    Once this is installed, VS Code will be available from the top menu.

1. Install Pylance. This is an extension for VS Code that provides Python language support. Refer to the [Pylance extension documentation](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance&WT.mc_id=academic-17441-jabenn) for instructions on installing this extension in VS Code.

## Hello world

It is traditional when starting out with a new programming language or technology to create a 'Hello World' application - a small application that outputs something like the text `"Hello World"` to show that all the tools are correctly configured.

The Hello World app for the Pi will ensure that you have Python and Visual Studio code installed correctly.

This app will be in a folder called `nightlight`, and it will be re-used with different code in later parts of this assignment to build the nightlight application.

### Task - hello world

Create the Hello World app.

1. Launch VS Code, either directly on the Pi, or on your computer and connected to the Pi using the Remote SSH extension

1. Launch the VS Code Terminal by selecting *Terminal -> New Terminal, or pressing `` CTRL+` ``. It will open to the `pi` users home directory.

1. Run the following commands to create a directory for your code, and create a Python file called `app.py` inside that directory:

    ```sh
    mkdir nightlight
    cd nightlight
    touch app.py
    ```

1. Open this folder in VS Code by selecting *File -> Open...* and selecting the *nightlight* folder, then select **OK**

    ![The VS Code open dialog showing the nightlight folder](../../../images/vscode-open-nightlight-remote.png)

1. Open the `app.py` file from the VS Code explorer and add the following code:

    ```python
    print('Hello World!')
    ```

    The `print` function prints whatever is passed to it to the console.

1. From the VS Code Terminal, run the following to run your Python app:

    ```sh
    python3 app.py
    ```

    > 💁 You need to explicitly call `python3` to run this code just in case you have Python 2 installed in addition to Python 3 (the latest version). If you have Python2 installed then calling `python` will use Python 2 instead of Python 3

    The following output will appear in the terminal:

    ```output
    pi@raspberrypi:~/nightlight $ python3 app.py
    Hello World!
    ```

> 💁 You can find this code in the [code/pi](code/pi) folder.

😀 Your 'Hello World' program was a success!
