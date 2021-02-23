# Face Recognition for Access Control 

The project allows to recognize in real-time video from webcam the faces of different people. Moreover with the identification, the user can register the correct access time to the office position.
The software executed on an embedding system, such as Raspberry Pi, can replace an old badge system based on sign papers or cards.
The GUI is developed using tkinter library and the logs are saved directly on text files.
Thanks to face recognition library: https://github.com/ageitgey/face_recognition

# INSTALLATION

The python3 script needs the following libraries:

* numpy >= 1.13.3
* opencv with extra modules (opencv-contrib-python) >= 4.1.1.26
* tkinter
* PIL >= 6.2.1

****

# LAUNCH

Before to launch you need to create a folder called people and then put it the face images that you want to recognize.

$ python3 face_tk_new.py 

It needs the execution of the python script and the following real-time identifcation.


****


# HOW IT WORKS?

At the startup of the python application, all the images from the people folder are loaded and the face encodings are generated.
These face encodings will be used to compare with the current ones generated during the real-time video.
After that, it's possibile to register a new access in the office clicking on the register button. The datetime is picked from the current system datetime.
With the second click on this button allows to register the access in the text file. 
In order to reduce the resources used by the python script the register function can be temporarily deactivated by clicking on the register button.


****

