# Smart-Attendance-System


Title: Face Recognition Attendance System with KNN and Text-to-Speech

Description:

This Python project implements a face recognition attendance system using the K-Nearest Neighbors (KNN) algorithm for classification. It leverages OpenCV, NumPy, pickle, scikit-learn, and a text-to-speech (TTS) library to capture training images, recognize faces during attendance recording, and store attendance records in CSV format. Optionally, you can integrate a graphical user interface (GUI) for a more user-friendly experience.

Features:

Captures training images for registered users. Recognizes faces using KNN classification during attendance recording. 
Saves attendance records in CSV format (date-specific files).
Provides text-to-speech confirmation of attendance (optional, requires additional setup). 
Optionally integrates a GUI (requires additional libraries). Getting Started:

Prerequisites:

Python 3.x OpenCV (pip install opencv-python) 
NumPy (pip install numpy) 
pickle (pip install pickle) 
scikit-learn (pip install scikit-learn) 
Text-to-speech library (e.g., pyttsx3: pip install pyttsx3) 
(Optional) GUI toolkit (e.g., Tkinter, PyQt) for the GUI win32com (pip install pywin32) 
Download the pre-trained Haar cascade classifier:

Download the haarcascade_frontalface_default.xml file from https://github.com/opencv/opencv/tree/master/data/haarcascades and place it in the same directory as your Python script. 
Run the script:

Training Process:

When the script starts, you'll be prompted to enter your name. Look at the camera, and the system will capture 100 images of your face at intervals.
This process will be repeated for any additional users you want to register. Attendance Recording:

Once training is complete, the system will switch to attendance recording mode. The camera will display detected faces. 
The KNN classifier will predict the most likely identity based on the training data. 
Recognized names will be displayed next to the faces. 
Text-to-speech will announce the recognized name upon pressing 'o'. The attendance record for the current user will be saved to a CSV file. 
Press 'q' to exit the program. Structure:

face_recognition_attendance_knn_tts.py 
# Main script haarcascade_frontalface_default.xml 
# Pre-trained face classifier (replace with actual filename if different) names.pkl 
# Stores user names (created during training) faces_data.pkl 
# Stores training face data (created during training) Attendance/ 
# Directory to store attendance CSV files (created if non-existent) 
# win32com.client  used for voice Notes:

This script assumes you have a webcam connected to your computer.
Modify the training image capture logic or data structure if you have a different approach for loading existing training data. 
Consider adding error handling and more informative user feedback for a robust system. 
You have to make an Attendance name folder in the current directory so that it can save attendance.csv files in it.
