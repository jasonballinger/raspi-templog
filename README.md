# Raspberry Pi CPU Temperature Log
[![CodeFactor](https://www.codefactor.io/repository/github/jasonballinger/raspi-templog/badge/master)](https://www.codefactor.io/repository/github/jasonballinger/raspi-templog/overview/master)
![.github/workflows/styleCheck.yml](https://github.com/jasonballinger/raspi-templog/workflows/.github/workflows/styleCheck.yml/badge.svg?branch=master&event=push)
<br>Created by Jason Ballinger, 2019
## Developer Notes
The code in this repository is loosely based off of the [Raspberry Pi Organization's Tutorial](https://projects.raspberrypi.org/en/projects/temperature-log). However, this code will be actively maintained and issues reported will be looked at.
## Report a Bug
To report a bug, click [here](https://github.com/jasonballinger/raspi-templog/issues), click "new issue" and choose "bug report". Please then fill out the template and describe the issues that you are having.
## Installation
You can install this code two ways. You can either clone the repository or install via **npm**. The directions for this are below.
### Before you start
Make sure that you have the python3 and python3-matplotlib packages installed. If you don't, open a Terminal window and type ```sudo apt-get install python3 python3-matplotlib -y```. Now you can continue.
### Install
1. First, you're going to need to open a terminal window. Then, type ```cd /home/pi/Documents```. After this, type ```git clone https://github.com/jasonballinger/raspi-templog```.
2. Secondly, type ```sudo crontab -e```. If you are asked, choose **nano** as your text editor. Scroll down to the bottom of this document and type ```@reboot python3 /home/pi/Documents/raspi-templog/templog.py```.
    * This is assuming that you have saved the cloned repository to your Documents folder, your username is "pi" and you haven't modified any file names.
## Tutorial
Now that you have installed the program, let's go ahead and teach you how to use it. By modifying the **crontab** document, you have made it so that the script will start on startup. If you would like to see the CPU Temperature data, just go ahead and open a Terminal window and type ```cat cpu_temp.csv```. If you would like to see a graph, go to your Terminal window and type ```mousepad /home/pi/Documents/raspi-templog/templog.py``` and uncomment line 32 or ```graph(temp)```.
### A quick reminder
If using Raspbian Jessie or previous, replace ```mousepad``` with ```leafpad```.
## Screenshots
No screenshots yet. Still working on getting those out.
## License
This code is licensed under the Unlicense. For more information, click [here](https://github.com/jasonballinger/raspi-templog/blob/master/LICENSE).
## Support Me
You can support me by making a donation through ko-fi. Click the button below to do so. Button not showing up? Click [here]().
<br><br>[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/I2I3WLST)
