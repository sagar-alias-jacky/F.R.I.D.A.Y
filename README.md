# Ironman-Friday-Virtual-Assistant

Note: This program currently runs only on Windows 10 machines.

A simple virtual assistant for windows written in python. It takes voice commands and right now can search Google, play YouTube videos, play music, get info from Wikipedia, give the weather data of any location in addition to some basic functionalities like getting the system date and time, time varying greetings on startup, and opening some specified websites(any website can be added by adding it in the .py script) etc.

For Commands, Additional Settings and Options, Common Issues and Solutions check the end of this README file.

Note: The voice commands and keywords are hard coded as of now. This system can be made more efficient with the use of sql database of commands and responses or even with the application of Machine Learning Principles to implement dynamic learning of new commands and responses.

Instructions for use:

*Prerequisites*

1. Have git installed on your local machine. (For installation instructions refer https://git-scm.com/)
2. Have python installed on your local machine (The one used for this project is version 3.9.2). (For installation instructions refer https://www.python.org/)

*Steps to get the project set up on your local machine*

1. Open the command prompt or powershell on your local machine and navigate to the directory where you want to set up the project. (If you have no idea how to do this check this out -> https://www.howtogeek.com/659411/how-to-change-directories-in-command-prompt-on-windows-10/)

2. Once you have navigated to your desired destination directory in the cmd, type in the following command:

   git clone https://github.com/sagar-alias-jacky/Ironman-Friday-Virtual-Assistant.git

   This fetches the repository from github and downloads it to your local machine in the destination directory you chose.

Note: If you are cloning into a virtual environment please make sure that all the contents inside the downloaded repository are cut and pasted in the same folder as the Lib folder in the virtual environment or else some packages may not be detected by the program when you run it.  

3. Now close out of the command prompt and navigate to the destination directory using the file explorer.

4. Open the file named FridayDavid.py in a text editor(preferably Visual Studio Code which can be downloaded from https://code.visualstudio.com/).

5. On line 25 of the FridayDavid.py replace the default path with the full path of your desired web browser installed on your machine. You can also change the variable names to match the browser you chose but be sure to change it in the whole file wherever it is used or referenced.

6. On line 78 and 79 replace the default path with the path of the files on your local machine. 

7. On line 135 replace the 'yourAPIkeyhere' with your own Open Weather API key. (If you don't have one yet you can get one at https://openweathermap.org/api for free of cost)

8. On line 236 you can modify the name at the end of the string to your name instead of the default.

9. On line 249 replace the default path with the path of the file on your local machine.

10. Open the command prompt once again and navigate to the downloaded repository directory and type in the following command:

    pip install -r requirements.txt

    Proceed to step 11 if it completes successfully without any errors, else check the end of this README file for solutions to some common errors.

11. Now type in the command:

    python FridayDavid.py 

    Your virtual assistant program should be running successfully now.

Note: If you cloned the repository into a virtual environment and have installed the packages from requirements.txt in the virtual environment, please make sure to activate the virtual environment before using the above command to run the program or else it will not work.

*Commands included in the program*

You can just skim through the FridayDavid.py file to see the commands which are included in the program. They should be pretty easy to find.

*Additional Settings and Options*

1. You can uncomment lines 32 through 39 in the FridayDavid.py file to get your program to display the sapi5 voices available in your system, when the program is run. You can note down the desired voice's index and use it in line 41.

Note: You can download and install additional sapi5 voices of your choice on your system from sites like http://www.zero2000.com for example. 

2. You can uncomment lines 43 through 45 and set the volume and rate(speed) of your virtual assistant according to your choice.

3. Uncomment line 102 to have your virtual assistant say that extra line when the program is run.
 
4. If you have even a little experience in python you can easily add new commands,responses or modify the existing ones by modifying the FridayDavid.py file.

Common issues and solutions:

1. The pyttsx3 module is throwing up errors
   Solution: Be sure that the pyaudio module is installed(https://pypi.org/project/PyAudio/) and also all the required dependencies mentioned in the pyttsx3 documentation(https://pypi.org/project/pyttsx3/).

2. The webbrowser module shows errors
   Solution: Check that the full correct path of the browser you want to use is specified in the .py script.

3. path not found errors
Solution: Check that all the hard coded paths in the py script are set correctly according to where you have the repository in your pc or laptop. The paths used in the py script are in accordance with the location of the project in my computer. This will vary according to where you have cloned this repository to in your computer. So take care of that.

4. If you have issues with installing the pyaudio module then after running the pip install -r requirements.txt in the cmd, run the command:

   pipwin install pyaudio

   This should install it correctly.

5. If you face any other errors there's a bunch of resources online to help you with it. (If you don't know where to start try https://stackoverflow.com/)
