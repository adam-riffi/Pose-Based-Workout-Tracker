# Pose-Based Workout Tracker (Prototype)

> A browser-based prototype that uses your webcam and real-time pose estimation to detect and count squats and kettlebell-style swings. Designed for offline use and simple deployment.

---

## 🎯 Overview

This project demonstrates how computer vision and lightweight machine learning models can be used to analyze physical exercise without any wearable devices. The app runs entirely in the browser and provides live feedback to the user during two types of exercises:

- **Squats**
- **Kettlebell swings**

---

## 🧠 Features

- 🔍 Real-time pose detection using **MoveNet Thunder**
- 📹 Uses your webcam (no installation or login required)
- 🔄 Toggle between **Squat Mode** and **Kettlebell Mode**
- ✅ Repetition counter with state-based logic
- 🔊 Audio feedback for good form and completed reps (`ding` / `rep`)
- 👤 Live skeleton overlay and debug mode
- 🌐 Fully offline — no backend, no data sent anywhere

---

## 🛠 Tech Stack

| Component         | Technology                        |
|------------------|------------------------------------|
| Pose Estimation  | [MoveNet Thunder (TF.js)](https://www.tensorflow.org/js)  
| Frontend         | HTML / CSS / Vanilla JS           |
| Sound Feedback   | HTML5 Audio API                   |
| Deployment       | Static server / Localhost         |

---

## 🚀 How to Run

### 🔗 Option A — Localhost (recommended)

Due to browser restrictions, webcam access **won’t work** with `file://` paths.

#### Step-by-step:

1. Make sure you have Python installed
2. Open a terminal in your project folder
3. Run: python -m http.server 8000
Open http://localhost:8000 in your browser

✅ Allow webcam access when prompted

📁 File Structure
bash
Copy
Edit
pose-workout-tracker/
├── index.html        # Main app logic and UI
├── ding.mp3          # Sound triggered on position change
├── rep.mp3           # Sound triggered on completed rep
├── README.md         # Project description and usage
🧪 Prototype Limitations
Only detects basic body pose, not external objects (no real kettlebell tracking)

Not trained to recognize incorrect form

Only supports one user at a time

Ghost pose overlay not included in this version

🧩 Extension Ideas
Add ghost pose comparison for form feedback

Export session data (CSV or JSON)

Mobile version (using Capacitor or TWA)

Gamification and visual feedback (stars, streaks, etc.)

Integrate with online video workout platforms

📌 Disclaimer
This is an early-stage prototype developed for research and experimentation.
It is not a medically certified tool and should not be used to assess real-world physical performance or health conditions.

🧑‍💻 Author
Created by Adam Riffi — 2025
Open to collaboration and feedback.
