# Forget-Me-Not Capstone Repository

This file contains information regarding the Forget-Me-Not capstone project[18-500 F25 Group A7], and each of its subcomponents.

## Project Pitch

The goal of this project is to essentially use Computer Vision models to tell users where they lost various objects around their house.

The key components are the array of cameras taking images, the models processing said images, the database storing said images, and the device that processes audio requests from users and ultimately tells the user where said object are.

As of right now, this is project is currently being developed though an MVP has been created that leverages an SQLite server running CNN/Transformer Models like Grounding DINO and YOLO to classify objects. In addition Open AI's whisper model is used to process audio input. 


Here is what is currently in each of our subdirectories:

- `Audio/`: This contains audio processing scripts and text to vec scripts so that one could more easily find the words they are looking for in the database.
- `CV-Algs/`:  This directory contains preprocessing scripts on camera input so that the costly CNN/Transformer Models don't have to be run on every image.
- `raspi-scripts/`: This directory contains basic scripts pertaining to raspberry-pis. This will likely include scripts that do things like periodically take photos, or record microphone data. The scripts in this directory will likely not be used in our final code. 
- `webserver/`: This directory contains all code pertaining to the webserver that our final application will be running on. Currently, it is in a very rudimentary state, and can only recieve/send files. Much more information is present inside of the directory's readme. NOTE: The wevserver has its own virtual enironment. Be sure to initialize it appropriately before running any code.
- `Yolo-Classification/`:  This directory contains all code for training and validating various object classification models obtained using YOLO.
- `GroundingDino/`: This directory contains the GroundingDino Classification Model and various testing scripts.

