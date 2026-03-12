
# Embedded Multilingual Speech Translation System using ESP32

A low-cost embedded speech translation system that captures spoken English using an ESP32 device and converts it into translated speech in Hindi or Telugu using speech recognition, translation, and text-to-speech synthesis.

The project demonstrates how **embedded devices can interact with AI services to build a speech-to-speech translation pipeline.**

---

## 📚 Project Overview

This project implements a multilingual speech translation system using an **ESP32 microcontroller** and AI-based speech processing tools.

The system captures spoken input from a microphone, converts speech to text using **Vosk speech recognition**, translates the recognized text, and generates translated speech that is played through a speaker connected to the ESP32.

### Supported Languages
- English → Hindi
- English → Telugu

### Key Concepts
- Embedded Systems
- Speech Recognition
- Natural Language Processing
- Edge + Server AI Architecture
- IoT Communication

---

## 🏗 System Architecture
ESP32 Microphone
│
▼
Audio Recording Module
│
▼
Speech Recognition Server
(Vosk STT)
│
▼
Translation Service
│
▼
Text-to-Speech Generation
│
▼
ESP32 Audio Playback
(Speaker)

Speech recognition runs using **Vosk**, while translation and speech synthesis are handled by server-side services.

---

## ⚙️ Workflow

1. User speaks English into the **INMP441 microphone** connected to the ESP32.
2. The ESP32 records audio using the **I2S interface**.
3. The recorded audio is sent to a **speech recognition server**.
4. Speech is converted into text using **Vosk STT**.
5. The text is translated into **Hindi or Telugu**.
6. A text-to-speech system generates translated audio.
7. The ESP32 downloads the generated audio and plays it through the **speaker**.

---

## 🧠 Technologies Used

### Hardware
- ESP32 Microcontroller
- INMP441 Digital Microphone
- MAX98357A DAC Amplifier
- 3W Speaker

### Software
- Python
- MicroPython
- Flask
- Vosk Speech Recognition
- gTTS / TTS Engine
- Translation API / Library

### Communication
- HTTP APIs
- Wi-Fi communication between ESP32 and server

---

## 🧩 Hardware Connections

### ESP32 Pin Connections

| Component         | ESP32 Pin       | Description                            |
|------------------|------------------|----------------------------------------|
| **INMP441 Mic**   |                  |                                        |
| VCC              | 3.3V             | Power                                  |
| GND              | GND              | Ground                                 |
| SCK              | GPIO 14          | Bit Clock                              |
| WS               | GPIO 15          | Word Select (L/R Clock)                |
| SD               | GPIO 32          | Serial Data (mic output)               |
| **MAX98357A DAC** |                  |                                        |
| VIN              | 5V               | Power                                  |
| GND              | GND              | Ground                                 |
| LRC              | GPIO 25          | L/R Clock                              |
| BCLK             | GPIO 26          | Bit Clock                              |
| DIN              | GPIO 22          | Digital Audio In from ESP32            |
| **Speaker**       | DAC Output       | 3W speaker connected to MAX98357A      |

---
### 🧠 ESP32 Circuit Diagram
![image](https://github.com/user-attachments/assets/12746648-dd57-489b-9a16-a2cb0dcb836d)
---

## 🔌 Hardware Setup

![Hardware Setup](https://github.com/user-attachments/assets/21991b89-627d-40d4-9688-4e84bf2a5bcf)

---


## Sample Output

Example console output from the system:

Recording audio...
Recording for 3 seconds

Sending audio to Vosk STT server...

Transcript:
hello how are you

Translating and fetching TTS...

Playing translated speech...


---

## 📊 Performance Metrics

Typical execution timing:

| Stage | Approx Time |
|------|-------------|
Audio Recording | ~3 seconds |
Speech Recognition | ~30-35 seconds |
Translation + TTS | ~2 seconds |
Audio Playback | ~2 seconds |

Total pipeline time: **~40 seconds**

The prototype prioritizes demonstrating the complete speech translation pipeline.  
Future improvements will focus on **latency reduction and edge processing**.

---

## 🎥 Demo

A working prototype demonstration video is included in the repository.

The demo shows:

1. Voice input captured by ESP32
2. Speech recognition processing
3. Translation into Hindi or Telugu
4. Audio playback through the speaker

---

## 📂 Project Structure
project/
│
├── app.py
├── config.py
├── record_audio_final.py
├── speech_to_text.py
├── text_to_speech.py
├── play_audio_final.py
├── server.py
├── translate_speak_server.py
├── wifi.py
│
├── demo/
│ └── demo_video.mp4
│
├── Documentation/
│ ├── PROJECT_REPORT.docx
│ ├── ResearchPaper.docx
│ ├── poster.pptx
│ └── presentation.pptx
│
├── requirements.txt
└── README.md


---

## 📄 Documentation

Supporting documentation is available in the **Documentation** folder:

- Project Report
- Research Paper
- Poster
- Presentation Slides

---

## 🚀 Future Improvements

- Reduce speech recognition latency
- Integrate fully offline translation models
- Add support for more languages
- Implement streaming speech recognition
- Optimize pipeline for edge devices

---

## 🧑‍💻 Author

Charul Pareek  
B.Tech Computer Science

---

## 📜 License

This project is released under the MIT License.




### 🧠 ESP32 Circuit Diagram
![image](https://github.com/user-attachments/assets/12746648-dd57-489b-9a16-a2cb0dcb836d)


## 🔌 Hardware Setup
![WhatsApp Image 2025-06-21 at 13 58 32_4b5ef713](https://github.com/user-attachments/assets/21991b89-627d-40d4-9688-4e84bf2a5bcf)










