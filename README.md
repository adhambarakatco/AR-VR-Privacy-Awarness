# Privacy-Aware AR Application

## 📖 Overview
This project, developed during a hackathon, aims to enhance **privacy awareness** using **Augmented Reality (AR)** and **Unity**. It educates users on safeguarding their personal data and detects and highlights privacy risks in real-world scenarios.

---

## 📽️ Demo Videos
- **Tool Mode**: [Insert link here]
- **Educational Mode**: [Insert link here]

---

## 🎯 Functionalities
### Tool Mode
- **Text Detection**: Extracts text from the environment using a camera or uploaded images.
- **Object Detection**: Identifies objects like passports, IDs, and other private items.
- **Recommendations**: Provides safer alternatives for detected sensitive information.

### Educational Mode
- **Interactive Gameplay**: Engages users in identifying private data. Correct identifications score points.
- **Virtual Mentor**: A fictional character provides personalized privacy tips and feedback.

---

## 🌐 System Architecture
The project comprises the following components:

### AR Integration
- **Object Detection**: Scans the environment to identify sensitive objects.
- **Enhanced Interactivity**: Includes 3D visualizations and gamified elements to improve user engagement.

### AI Model
- Analyzes extracted text for privacy risks.
- Recommends safer textual variations for detected sensitive data.

---

## 🖥️ Server Details
The server plays a critical role in the system by handling the backend processes. It is built using **Flask** and supports the following APIs:

### 1. **Text Extraction API**
- **Endpoint**: `/extract-text`
- **Method**: POST
- **Input**: Accepts image files (e.g., PNG, JPEG) uploaded via multipart form data.
- **Output**: Extracted text from the image using Tesseract OCR.

### 2. **Privacy Violation Detection API**
- **Endpoint**: `/detect-violations`
- **Method**: POST
- **Input**: Text provided as JSON.
- **Output**: A list of detected privacy violations categorized into Personally Identifiable Information (PII) and Sensitive Personal Information (SPI).

### 3. **Recommendation System API**
- **Endpoint**: `/suggest-solutions`
- **Method**: POST
- **Input**: JSON containing detected violations.
- **Output**: Suggested solutions and safer alternatives for the violations.

### Key Features
- **Tesseract OCR**: Extracts text from images to process and analyze potential privacy risks.
- **Regex Matching**: Detects sensitive information like emails, phone numbers, Social Security Numbers, and more.
- **AI-Powered Recommendations**: Generates alternative text or suggestions for detected violations to protect privacy.
- **Cross-Origin Resource Sharing (CORS)**: Allows seamless integration with the front-end Unity app.

### How to Run the Server
1. Install the dependencies using `requirements.txt`:
   ```bash
   pip install -r requirements.txt
   ```
2. Start the server:
   ```bash
   python app.py
   ```
3. Access the APIs locally at `http://127.0.0.1:4444` or deploy the server using **Vercel** (configured with `vercel.json`).

---

## 🛠️ How to Set Up and Run
### Prerequisites
- **Unity Engine**: Version X.X or higher.
- **Python**: Version X.X or higher.
- **Dependencies**: Install Python packages using `requirements.txt`.

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/adhambarakatco/AR-VR-Privacy-Awareness.git
   cd AR-VR-Privacy-Awareness
   ```
2. Install server dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the server:
   ```bash
   python app.py
   ```
4. Open the Unity project and build it for your preferred platform.

---

## 🏗️ Technology Stack
- **Unity**: AR integration and gamification.
- **Python (Flask)**: Server-side logic and API development.
- **Tesseract OCR**: Text extraction from images.
- **spaCy**: Natural language processing for privacy analysis.

---

## 📈 Future Work
- **Metaverse Integration**: Expanding the app to safeguard user privacy in virtual environments.
- **Advanced AI**: Enhancing detection and recommendation capabilities with deep learning.
- **New Features**: Additional gamified experiences and privacy tutorials.

---

## 📄 License
*(Specify license here, e.g., MIT, Apache 2.0.)*
