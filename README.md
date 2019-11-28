# Raspberry Pi CPU Temperature Log
[![CodeFactor](https://www.codefactor.io/repository/github/jasonballinger/raspi-templog/badge/master)](https://www.codefactor.io/repository/github/jasonballinger/raspi-templog/overview/master)
<br>Created by Jason Ballinger, 2019
## Developer Notes
This is a section for notices that I put out. I will link all of these notices to issues and remove them from this README when an issue is closed.
### Github Actions CI not working
I am still working on setting up the CI for this repository and I have run into a few problems. I am coming from Travis CI and I am just working on getting some things set up. I should be able to get this out soon. The issue for this notice is #2 and can be found [here](https://github.com/jasonballinger/raspi-templog/issues/2).
## Installation
You can install this code two ways. You can either clone the repository or install via **npm**. The directions for this are below.
### Before you start
Make sure that you have the python3 and python3-matplotlib packages installed. If you don't, open a Terminal window and type ```sudo apt-get install python3 python3-matplotlib -y```. Now you can continue.
### Cloning the repository
To clone the repository, you have two options.
#### Downloading & Installing a ZIP Archive
1. Navigate [here](https://github.com/jasonballinger/raspi-templog), click "Clone or Download" --> "Download ZIP" and save the .zip Archive to your Raspberry Pi's "Documents" folder. Then, unzip the archive and you're *almost* good to go.
2. Next, open a terminal window. Type ```sudo crontab -e```. If asked, choose **nano** as your editor. Then, scroll to the bottom and type ```@reboot python3 /home/pi/Documents/raspi-templog/templog.py```.
    * This is assuming that you have saved the cloned repository to your Documents folder, your username is "pi" and you haven't modified any file names.
#### Installing via Terminal
1. First, you're going to need to open a terminal window. Then, type ```cd /home/pi/Documents```. After this, type ```git clone https://github.com/jasonballinger/raspi-templog```.
2. Secondly, type ```sudo crontab -e```. If you are asked, choose **nano** as your text editor. Scroll down to the bottom of this document and type ```reboot python3 /home/pi/Documents/raspi-templog/templog.py```.
    * This is assuming that you have saved the cloned repository to your Documents folder, your username is "pi" and you haven't modified any file names.
### Installing via pip
I haven't set up the ```pip``` package yet. I will update this README when I have.
## Tutorial
Now that you have installed the program, let's go ahead and teach you how to use it. By modifying the **crontab** document, you have made it so that the script will start on startup. If you would like to see the CPU Temperature data, just go ahead and open a Terminal window and type ```cat cpu_temp.csv```. If you would like to see a graph, go to your Terminal window and type ```mousepad /home/pi/Documents/raspi-templog/templog.py``` and uncomment line 32 or ```graph(temp)```.
## Code Breakdown
I didn't really comment my code this time around, so here's a little bit of a breakdown. Lines 1-3 are just imports, so nothing really fancy. Line 5 is a variable making it so that the code doesn't stretch all over the screen and I can type ```cpu``` instead of ```CPUTemperature``` Lines 7-9 initialize the plotting mechanism. Lines 11-13 log the data to a CSV file. Lines 15-21 graph the data and 23-27 is a while loop that keeps this all running. Line 26 is commented out by default. But, if you would like to see a graph instead of a line, go ahead and uncomment that. This log updates every second (1000 milliseconds).
## Screenshots
No screenshots yet. Still working on getting those out.
## License
This code is licensed under the Unlicense. For more information, click [here](https://github.com/jasonballinger/raspi-templog/blob/master/LICENSE).
## Support Me
You can support me by making a donation through ko-fi. Click the button below to do so. Button not showing up? Click [here]().
<br>[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/I2I3WLST)
