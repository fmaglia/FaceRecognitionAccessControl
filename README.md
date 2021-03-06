# Face Recognition for Access Control 

The project allows to recognize in real-time video from webcam the faces of different people. Moreover with the identification, the user can register the correct access time to the office position.
The software, executed on an embedding system (such as Raspberry Pi), can replace an access system based on badges.
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

The system can be boosted using CNN: for doing this you need to modify the face_locations function as below.

`face_locations = face_recognition.face_locations(small_frame, model="cnn")`

Obviously, the performance will be reduced highly increasing the number of faces to recognize.


****


# HOW IT WORKS?

At the startup of the python application, all the images from the people folder are loaded and the face encodings are generated.
These face encodings will be used to compare with the current ones generated during the real-time video.
After that, it's possibile to register a new access in the office clicking on the register button. The datetime is picked from the current system datetime.
To register an access you need to firstly click on the register button to activate the face identification and then re-click it again to register the office access.
In order to reduce the resources used by the python script the register function is temporarily deactivated after the correct registration procedure.



****

