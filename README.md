# PentaHack
This repository contains the relavent files used to conduct a computer vision(CV) analysis on the driver's habits. It should primarily used to assist in the inexperienced driver or trainee drivers to learn and master driving.

## Technic used
### -Background subtraction
Done using optical flow. Initial implentation uses menual background subtraction. openCV and greyscale conversion are used to conduct background subtraction. The input video are saperated into different frames and compare the differences. This is removed and optical flow is used instead.

### -Optical flow
Estimate the movement of object in the video. This is used inplace of background subtraction. If the object is not in the previouse frame, the code computes the magnitude and angles of the optical flow using the CV2.cartToPolar.

### -AES encryption
pycryptodome Crypto.Cipher import AES were used to encrypt the output numpy file. It is saved using numpy.save() method. CV2.imwrite is used to create the directory which stores the images

## Running the file
### Steps to run the file
1. Download the assets folder
2. Ensure the folder is in the same directory as the notebook
3. Ensure the train.mp4 is in the assets folder
4. Uncommand and install the pycryptodome and opencv-python file before running the notebook
5. Run the notebook in jupyternotebook environment
6. To generate the output, please ensure that the entire video is ran before encrption and decryption.

### Screenshot of the optical flow output
![screenshot](https://github.com/adityavp99/PentaHack/blob/main/output/image.png?raw=true)

## Origin of data
### Source of the video
The training video was obtained from the public dataset of D²-City: A Large-Scale Dashcam Video Dataset of Diverse Traffic Scenarios. It is availiable online in the [science data bank](https://www.scidb.cn/en/detail?dataSetId=804399692560465920)

### Source of the lane marking
The size and length of the lane marking were obtained from the [Hainan government in China](http://www.orac.hainan.gov.cn/ggxxbzml2016/GB5768.3-2009.pdf). This is selected as the training video is by a ride hailing company named DiDi in China.
