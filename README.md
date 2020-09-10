# Optical mark recognition using OpenCV

![alt text](https://github.com/sakethbachu/OMR-scanner/blob/master/Img/omr%20demo.jpg "Logo Title Text 1")

## Description
Optical Mark Recognition, or OMR for short, is the process of automatically analyzing human-marked documents and interpreting their results. Bubble sheets are the easily understandable and interpretable versions of the OMR. They are usually used as exam sheets, where students fill in the bubble which corresponds to an option of a multiple choice question. This was built for [NEO](https://neo.ecellvnit.org/) ( National Entrepreneurship Olympiad) conducted by the [E-Cell-VNIT](https://www.ecellvnit.org/).

## Method
There was a requirement of checking huge volume of papers without actually wasting precious human time. So, the aim was to build a bubble sheet scanner and test grader using Python and OpenCV. The brief steps that were taken to build this:
  1. Detect the exam-sheet in an image.
  2. Apply a perspective transform to extract the top-down, birds-eye-view of the exam.
  3. Extract the set of bubbles (i.e., the possible answer choices) from the perspective transformed exam.
  4. Sort the questions/bubbles into rows.
  5. Determine the marked (i.e., “bubbled in”) answer for each row.
  6. Lookup the correct answer in our answer key to determine if the user was correct in their choice.
  7. Repeat for all questions in the exam-sheet.

## Features
This system requires you to gather all your omr-sheets in one folder, with a click of one button, the pipeline will perform the above mentioned steps on every sheet and you will get the marks with the respective roll number of the student in an excel sheet, bringing the entire stats at one place.

## OMR sheet
The below shown sheet was used for conducting the prelims of the exam.
The first three rows represent the roll number of the student and the rest bubbles are for marking he answers.

![alt text](https://github.com/sakethbachu/OMR-scanner/blob/master/Img/Screenshot%20(206).png "Logo Title Text 1")

## Contents of this repository
1. Img : Contains the descriptive images and the omr-sheet.
2. omr_paper1.py : The python script used for evaluation.

## Requirements
1. Python
2. OpenCv

## Usage
Use this in command line where python is installed
`python omr.py --image images/imagename.png`

## Demo
![alt text](https://github.com/sakethbachu/OMR-scanner/blob/master/Img/test.jpeg "Logo Title Text 1")
