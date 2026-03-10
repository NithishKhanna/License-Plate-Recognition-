# License Plate Recognition System

This project implements an **Automatic License Plate Recognition (ALPR)** system using computer vision and optical character recognition. The system detects a vehicle's license plate from an image and extracts the license number using OCR.

## Overview

The program processes vehicle images to:

* Detect license plates using a Haar Cascade classifier
* Extract the license plate region
* Preprocess the image for better recognition
* Read the plate number using OCR
* Identify the Indian state based on the license plate prefix

## Technologies Used

* Python
* OpenCV
* NumPy
* Tesseract OCR
* PIL (Python Imaging Library)

## Required Libraries

Install the required libraries using:

```
pip install opencv-python numpy pytesseract pillow
```

## Tesseract OCR Installation

Download and install **Tesseract OCR**.

Example path used in this project:

```
C:/Program Files (x86)/Tesseract-OCR/tesseract.exe
```

Update the path in the code if needed.

## Project Files

```
License-Plate-Recognition
│
├── main.py
├── haarcascade_russian_plate_number.xml
├── car_img.png
└── Result.png
```

## How It Works

1. The image is loaded using OpenCV.
2. It is converted to grayscale.
3. Haar Cascade classifier detects the license plate region.
4. The plate area is cropped and preprocessed.
5. Tesseract OCR extracts text from the plate.
6. The system identifies the vehicle's state based on the prefix.

## Example

Input Image:

```
car_img.png
```

Output:

* Detected license plate
* Extracted license number
* Saved result image: `Result.png`

## State Identification

The program maps the first two characters of the license plate to Indian states.

Example:

```
TN → Tamil Nadu
KA → Karnataka
MH → Maharashtra
DL → Delhi
```

## Author

Nithish Khanna

## Future Improvements

* Real-time license plate recognition using webcam
* Support for video streams
* Deep learning based plate detection
* Improved OCR accuracy
