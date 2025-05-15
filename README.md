# Real-Time Emotion Detection & Sentiment Analysis System 🤖🎭

This project uses deep learning and computer vision to detect human emotions in real-time from facial expressions and responds through an Arduino-controlled system using LEDs or sound. Built with **Keras**, **OpenCV**, and **Arduino**, this interactive AI system bridges the gap between emotional recognition and physical feedback.

---

## 💡 Features
- 🎥 Real-time emotion detection using webcam
- 🧠 Emotion classification using CNN trained with Keras
- 📦 Face detection using Haar Cascade (OpenCV)
- 🔌 Arduino integration for physical feedback (e.g., lights, sounds)
- 🎯 Supports 7 emotions: Angry, Disgust, Fear, Happy, Neutral, Sad, Surprise

---

## 🛠️ Tech Stack

| Component      | Technology        |
|----------------|------------------|
| Model Training | Keras, TensorFlow |
| Video Capture  | OpenCV            |
| Emotion Labels | CNN Model         |
| Hardware I/O   | Arduino + PySerial|

---

## 🚀 How It Works

1. **Face Detection**: Uses OpenCV's Haar cascade to detect faces from the webcam feed.
2. **Preprocessing**: Grayscale face image is resized to 48x48 pixels and normalized.
3. **Emotion Prediction**: A CNN model classifies the emotion.
4. **Arduino Interaction**: Corresponding command is sent over serial to Arduino for physical feedback (like lighting an LED or sounding a buzzer).

---

## 📁 Project Structure

```bash
.
├── main.py                     # Main script for live detection
├── sssupermodel.h5            # Pre-trained CNN model
├── haarcascade_frontalface_default.xml  # Face detection classifier
├── Sentiment_Detection.ino    # Arduino sketch to control outputs
└── README.md                  # Project documentation
# Real time Emotion Detection and sentiment analysis

🖥️ Getting Started
Requirements
Python 3.7+

OpenCV

Keras & TensorFlow

NumPy

PySerial

Arduino IDE

Install Dependencies
pip install opencv-python keras tensorflow pyserial numpy
Run the Project
Upload Sentiment_Detection.ino to Arduino using the Arduino IDE.

Adjust the COM port in main.py to match your system.

Run the main script:
python main.py
Press Q to quit the application.

🔧 Arduino Mapping
Each emotion is mapped to a single character command:

Emotion	Command	Output (example)
Angry	A	Red LED / Alarm
Disgust	D	Green LED
Fear	F	Blue LED
Happy	H	Yellow LED
Neutral	N	White LED
Sad	S	Soft buzzer tone
Surprise	X	Flashing lights

📷 Sample Output
(Insert your own screenshot if desired)

🧠 Future Improvements
Add audio sentiment analysis

Enhance model accuracy with larger datasets

Web-based version using Flask/Streamlit

Emotion-based ambient lighting systems

📜 License
This project is under the MIT License.

🙌 Acknowledgements
Keras Documentation

OpenCV Docs

FER2013 Dataset

