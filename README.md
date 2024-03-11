# aICanSee - Application for the Visually Impaired

## Overview
aICanSee is an innovative application designed to provide assistance and support for visually impaired individuals. 
Leveraging the power of AI, this application offers various features to enhance the daily lives of users.

## Features

### GUI Development
The tkinter library is used for creating the graphical user interface (GUI) of the application. Buttons are defined for different functionalities, making the app user-friendly.

### 1. Weather Suggestions
- Get real-time weather updates for your location(The geocoder library is used to obtain the current location)
- Receive outfit suggestions based on current weather conditions.(Used OpenWeather's user-friendly weather API's: https://openweathermap.org/api)
- Convert weather information and suggested outfit information from text to speech(Used gTTS [Google Text-to-Speech] library to convert text to speech)
### 2. Capture and Send
- Capture images with a double-tap for various purposes.
- Automatically send to email id (Used app passwords: https://support.google.com/accounts/answer/185833?hl=en)
- The smtplib library is utilized to send captured images via email.
- Utilize OCR to extract text content from images(Used the pytesseract library integrates with the Tesseract OCR engine to extract text content from captured images.)
### 3.Find Color
- Analyze dominant colors in captured images for helping blind understand and choose their outfit.
- Many applications for blind are based on volunteer helping people.
- This feature will help them identify the color of a dress.
- The K-Means clustering algorithm, implemented using OpenCV, is utilized to find the dominant color(s) in the captured images.  
### 4. Helpme
- Send emergency messages with your current location to predefined contacts.
- This is implemented by using whatsapp links and location data, to contact your guardian.
- You can use other SMS or paid services.
- 
### 5. Object Recognition
- Capture an image and receive spoken descriptions of objects in the image.(TensorFlow is used along with a pre-trained model from TensorFlow 
   Hub (tfhub.dev) for object recognition.)
- This allows the application to describe objects captured by the camera.
- Enhance accessibility with object recognition technology.
- You can also make use of image -to- text pretrained models from hugging face for image captioning 
  (https://huggingface.co/docs/transformers/main/en/tasks/image_captioning)
  
### 6. Emergency Assistance
- Trigger an emergency alarm with a triple-tap for immediate attention.
- The pygame library is used for playing audio files, including the generated speech and alarm sounds.

## Getting Started
### To use aICanSee, follow these steps:
#### Set up API keys and credentials:
1. OpenWeatherMap API key for weather updates.
2. Gmail credentials for image sharing via email.
3. Replace placeholder values in the code:
   - Replace add_api_key_here with your OpenWeatherMap API key.
   - Update sender_email, sender_password, and receiver_email with your email credentials.
### Run the application:
`python ai_can_see.ipynb`

## Usage
Execute the weather suggestion feature with the "1. Weather" button.
Capture and send images with the "2. Capture and Send" button (double-tap to capture).
Find dominant colors in images with the "3. Find Color" button.
Request emergency assistance with the "4. Help Me" button.
Use the "5. Tell me the object?" button for object recognition.
Trigger an emergency alarm with the "6. Emergency Alarm" button (triple-tap to activate).
