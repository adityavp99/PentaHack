# PentaHack
This repository contains the relevant files for conducting a computer vision(CV) analysis of drivers' habits. It should primarily be used to assist inexperienced drivers or trainee drivers in learning and mastering driving.

## Techniques used
### -Background subtraction
It was done using optical flow. Initial implementation uses manual background subtraction. openCV and greyscale conversion are used to conduct background subtraction. The input video is separated into different frames, and compare the differences. This is removed, and optical flow is used instead.

### -Optical flow
Estimate the movement of objects in the video. This is used in place of background subtraction. If the objects are not in the previous frame, the code computes the magnitude and angles of the optical flow using the CV2.cartToPolar.

### -AES encryption
pycryptodome Crypto.Cipher import AES were used to encrypt the output numpy file. It is saved using numpy.save() method. CV2.imwrite is used to create the directory which stores the images

## Running the file
### Steps to run the file
1. Download the assets folder
2. Ensure the folder is in the same directory as the notebook
3. Ensure the train.mp4 is in the assets folder
4. Uncommand and install the pycryptodome and opencv-python file before running the notebook
5. Run the notebook in the jupyternotebook environment
6. To generate the output, please ensure that the entire video is run before encryption and decryption.

### Front end design
Due to the time constrains the front end of the application was not connected to the model. A [prototype](https://www.figma.com/proto/7EvAccI8axL4IwiPkb8yEc/Driving-AI?node-id=1-13&scaling=scale-down&page-id=0%3A1&starting-point-node-id=1%3A13) was design instead with base functionalities. A video denmostrating the flow of the app can be found in the repository. It can be accessed here: https://github.com/adityavp99/PentaHack/main/DrivingAI_APP.mp4

### Screenshot of the optical flow output
![screenshot](https://github.com/adityavp99/PentaHack/blob/main/outputs/image.png?raw=true)

## Origin of data
### Source of the video
The training video was obtained from the public dataset of D²-City: A Large-Scale Dashcam Video Dataset of Diverse Traffic Scenarios. It is available online in the [science data bank](https://www.scidb.cn/en/detail?dataSetId=804399692560465920)

### Source of the lane marking
The size and length of the lane marking were obtained from the [Hainan government in China](http://www.orac.hainan.gov.cn/ggxxbzml2016/GB5768.3-2009.pdf). This was selected as the training video by a ride-hailing company named DiDi in China.
