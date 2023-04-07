# PentaHack
This repository contains the relavent files used to conduct a computer vision(CV) analysis on the driver's habits. It should primarily used to assist in the inexperienced driver or trainee drivers to learn and master driving.

## Technic used
### -Background subtraction
Done using optical flow. Initial implentation uses menual background subtraction. openCV and greyscale conversion are used to conduct background subtraction. The input video are saperated into different frames and compare the differences. This is removed and optical flow is used instead.

### -Optical flow
Estimate the movement of object in the video. This is used inplace of background subtraction. If the object is not in the previouse frame, the code computes the magnitude and angles of the optical flow using the CV2.cartToPolar.

### -AES encryption
pycryptodome Crypto.Cipher import AES were used to encrypt the output numpy file. It is saved using numpy.save() method. CV2.imwrite is used to create the directory which stores the images
