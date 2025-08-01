

# 🔔 Violence Alert System (Final Year Project)

A real-time **Violence Detection System** built using deep learning, image processing, and cloud-based services. This project uses a pretrained **MobileNetV2** model for detecting violent activity in live video streams. It also features a Telegram-based alert system and stores data securely in **Firebase Cloud Firestore**.

---

## 🧠 System Architecture

The system is divided into 6 modular stages, each responsible for a critical part of the detection and alerting pipeline.

---

### ✅ Stage 1: Human Detection
- Implemented using **Faster R-CNN Inception V2 COCO model**.
- Real-time person detection from video stream.
- Compared three pretrained models to balance **accuracy and inference speed**.

---

### ✅ Stage 2: Violence Detection
- Used **MobileNetV2** pretrained model to classify violence in video frames.
- Real-time predictions with **OpenCV overlays** indicating results.
- Training and testing datasets, scripts, and example videos are included.

---

### ✅ Stage 3: Telegram Alert System
- A Telegram bot integrated into a group for sending real-time alerts.
- On detecting violence, the **30th positive frame** is sent with:
  - 🕒 Timestamp
  - 🌐 Location
  - 📷 Camera ID
- Ensures timely action by authorities.

---

### ✅ Stage 4: Image Enhancement
- Uses **PIL (Python Imaging Library)** to enhance detected frames:
  - Sharpness and color improved by a factor of 1.2.
- Enhanced image is then sent via the Telegram bot.

---

### ✅ Stage 5: Face Detection
- Detected violent frame is scanned for **faces using MTCNN**.
- All faces are extracted and compiled into a single summary image.
- Sent through the bot for visual records of involved individuals.

---

### ✅ Stage 6: Firebase Integration
- Stores all critical data in **Cloud Firestore**:
  - Date, location, and image metadata.
  - Violence frame and face detection image as **Firebase Storage URLs**.
- Data access restricted to **authorized personnel** only.

---

## 📁 Project Structure

Violence_detection_model/
├── datasets/ # Training/testing video data
├── models/ # Pretrained MobileNetV2 weights
├── firebase_config/ # Firebase setup and credentials
├── telegram_bot/ # Bot config and message handlers
├── main.py # Main real-time detection pipeline
├── train_model.py # Training script for violence detection
├── requirements.txt # Python dependencies
└── README.md # Project documentation


---

## ⚙️ Technologies Used

- Python, OpenCV
- MobileNetV2, Faster R-CNN
- TensorFlow / PyTorch (specify as needed)
- MTCNN (Face detection)
- PIL (Image enhancement)
- Telegram Bot API
- Firebase Firestore & Storage

---

## 🚀 Getting Started

### 1. Clone the Repo
```bash
git clone https://github.com/PRANAVKAKDE613/Violence_detection_model.git
cd Violence_detection_model

 Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
3. Run the Model
bash
Copy
Edit
python main.py
Configure your Firebase and Telegram bot credentials before running.

📦 Dataset
This project can use:

RWF-2000

Hockey Fight Dataset

Custom surveillance datasets

🔐 Security & Access
Firebase data access is restricted to authenticated officials only.

Telegram group managed by authorized supervisors.

📜 License
This project is part of an academic submission and is shared for learning and demonstration purposes. For use in real-world deployments, proper dataset licensing and ethical use reviews are advised.

🙏 Acknowledgments
RWF-2000

Google Firebase

OpenCV & Python ecosystem

Telegram Bot API

📌 Project Completed ✅

python
Copy
Edit

---

Let me know if you'd like:
- A `requirements.txt` generated automatically
- Help adding badges (build, license, etc.)
- The actual architecture diagram embedded via Markdown

You're ready to commit this:
```bash
echo "[README content]" > README.md
git add README.md
git commit -m "Add detailed README"
git push









