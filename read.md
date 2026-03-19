# ✊✋✌️ Rock Paper Scissors Hand Gesture Recognition

An interactive **Rock Paper Scissors** game built with **Java**, **JavaFX**, and **TensorFlow**, powered by **real-time hand gesture recognition** through a webcam.

This project combines **computer vision** and **machine learning** to turn hand gestures into playable game moves. Instead of clicking buttons, players can show **rock**, **paper**, or **scissors** directly in front of the camera and let the model predict the gesture in real time.

---

## 📌 Overview

This application uses a trained image classification model to detect hand gestures captured from a webcam.  
The predicted gesture is interpreted as the player's move, then compared against a randomly generated move from the computer to determine the result of the game.

The model was trained using **Teachable Machine** and exported as a **TensorFlow SavedModel**, then integrated into a Java-based desktop application.

---

## 🚀 Features

- Real-time webcam-based gesture recognition
- Rock, Paper, Scissors gameplay
- TensorFlow model integration in Java
- JavaFX graphical user interface
- Custom-trained hand gesture dataset
- Prediction label mapping from exported model files

---

## 🛠️ Tech Stack

- **Java**
- **JavaFX**
- **Maven**
- **TensorFlow SavedModel**
- **Teachable Machine**
- **Computer Vision**

---

## 📂 Project Structure

```text
src/
└── main/
    ├── java/
    │   └── com/
    │       └── codedotorg/
    │           ├── model/
    │           │   ├── saved_model.pb
    │           │   ├── labels.txt
    │           │   └── variables/
    │           ├── modelmanager/
    │           │   ├── CameraController.java
    │           │   ├── ModelManager.java
    │           │   ├── ModelPredictor.java
    │           │   ├── ModelProcessor.java
    │           │   └── Prediction.java
    │           ├── App.java
    │           ├── GameLogic.java
    │           ├── GameOverScene.java
    │           ├── Loading.java
    │           ├── MainScene.java
    │           └── RockPaperScissors.java
    └── resources/
        └── com/
            └── codedotorg/
                └── styles.css
```
## ⚙️ How It Works

1. The webcam captures the player's hand gesture.
2. The image is processed before being passed into the model.
3. The TensorFlow model predicts one of the gesture classes:
- Rock
- Paper
- Scissors
4. The predicted label is cleaned and matched to the game logic.
5. The computer generates its own move.
6. The application displays the winner in the JavaFX interface.
