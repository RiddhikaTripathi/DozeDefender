# DozeDefender: Student Vigilance System

## 📖 Overview
**DozeDefender** is a real-time **drowsiness and yawn detection system** built using **Python**, **OpenCV**, **Dlib**, and **Pygame**.  
The project monitors a user’s eyes and mouth through a webcam feed to detect early signs of sleepiness such as prolonged eye closure and yawning.  
When drowsiness is detected, an alert sound is played to wake the user — making it especially useful for drivers, students, and professionals who spend long hours in front of screens.

---

## 🧠 Core Idea
The system uses the **Eye Aspect Ratio (EAR)** and **lip distance** as key visual indicators.  
When the EAR drops below a set threshold or a wide yawn is detected, the program triggers an audio alert.

---

## ⚙️ Technologies Used
- **Python 3**
- **OpenCV** – for real-time image and video processing  
- **Dlib** – for facial landmark detection  
- **Imutils** – for utility functions and video streaming  
- **Pygame** – for sound alerts  
- **Matplotlib** – for live plotting of EAR (Eye Aspect Ratio)

---

## 🧩 Features
✅ Real-time eye and mouth monitoring through webcam  
✅ Detects eye closure and yawning  
✅ Plays an alarm sound automatically when fatigue is detected  
✅ Displays a live graph of the **Eye Aspect Ratio** over time  
✅ Multi-threaded alert system for continuous monitoring  

---

## 🗂️ Project Structure
DozeDefender/
├── doze_defender.py # Main program file
├── shape_predictor_68_face_landmarks.dat # Facial landmark model
├── example_WAV_1MG.wav # Alert sound for drowsiness
├── mixkit-classic-alarm-995.wav # Alert sound for yawning
└── README.md # Project documentation


## ⚙️ How to Run

1. **Install dependencies:**
   ```
   pip install opencv-python dlib imutils pygame numpy matplotlib
   ```
2. **Download the facial landmark predictor:**
You can get shape_predictor_68_face_landmarks.dat from Dlib’s model page.
3. Run the project:
``` 
python doze_defender.py
```
4. Press q to quit the program.

## ⚡ How It Works
The webcam captures live video frames.
Facial landmarks are detected using Dlib’s 68-point model.
The Eye Aspect Ratio (EAR) is computed to check for eye closure.
The Lip Distance is computed to detect yawning.
If either value exceeds the threshold, an alarm sound is played via Pygame.
A live graph of EAR values is displayed alongside the video stream for visualization.

## 📊 Parameters Used
Parameter	Description	Default
EYE_AR_THRESH	Threshold below which eyes are considered closed	0.3
EYE_AR_CONSEC_FRAMES	Number of consecutive frames below threshold before triggering alarm	30
YAWN_THRESH	Minimum lip distance to detect yawning	20

🧑‍💻 Author
Riddhika Tripathi

