📘 **Smart Attendance System (AI + ML + MERN + DevOps)**

An AI-powered smart attendance system that uses **Real-time Face Recognition** to automatically detect a person and store attendance in a secure database.
This project demonstrates **Machine Learning, Full-Stack Development, Microservices, DevOps, Docker, and Cloud deployment concepts**.

---

# 🚀 **Features**

* 🎯 **Real-time Face Recognition** using Python + OpenCV + face_recognition
* 🤖 **ML Microservice** exposed as a Flask REST API
* 🗄️ **Backend API** built with Node.js + Express
* 💾 **Attendance stored in MongoDB**
* ⚡ **React Frontend Dashboard** (real-time updates)
* 🐳 **Containerized with Docker**
* ☸️ **Deployable on Kubernetes**
* 🔄 **CI/CD using GitHub Actions**

---

# 🆕 **NEW FEATURE: Liveness Detection (Anti-Spoofing)**

To prevent users from cheating the system using **passport photos, printed photos, or mobile screens**, the project now includes **Liveness Detection**.
Attendance is marked **only if a real human is detected**.

### ✔ Blink Detection (EAR – Eye Aspect Ratio)

* Detects natural blinking using facial landmarks
* Fake images/screens do not blink
* If EAR < **0.20**, blink is detected → **Real human**

### ✔ Head Movement Detection (Micro nose movement)

* Detects left/right micro head movements
* Photos/screens remain perfectly still
* If nose keypoints shift > **5px**, movement detected → **Real human**

### ✔ Final Rule

```
If (blink detected OR head movement detected):
      → Allow face recognition + save attendance
Else:
      → Return "Spoof Detected" (no attendance saved)
```

**Example Output when spoofing:**

```json
{
  "name": "Spoof Detected",
  "time": ""
}
```

---

# 🧠 **System Architecture**

```
+---------------------+        +----------------------+        +---------------------+
|  Face Recognition   | -----> |   Node.js Backend    | -----> |     MongoDB         |
|  (Python + Flask)   |        |   (API + Mongoose)   |        |  (Database Storage) |
+---------------------+        +----------------------+        +---------------------+
                                     ↑
                                     |
                              React Frontend
                           (Live Attendance View)
```

---

# 📁 **Project Structure**

```
attendance/
│
├── backend/               → Node.js + Express + MongoDB REST API
│   ├── src/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── app.js
│   │   └── server.js
│   ├── .env
│   └── package.json
│
├── ml/                    → Machine Learning microservice
│   ├── known_faces/
│   ├── app.py             → Flask API
│   ├── recognizer.py      → Face detection & encoding
│   ├── encode_faces.py
│   └── requirements.txt
│
├── fronted/ (or frontend) → React.js dashboard
│   └── src/App.js
│
└── README.md
```

---

# 🧪 **Tech Stack**

### **Machine Learning**

* Python
* OpenCV
* face_recognition library
* Flask API

### **Backend**

* Node.js
* Express.js
* MongoDB
* Mongoose

### **Frontend**

* React.js
* Axios
* Modern UI Table

---

# 🔥 **How to Run the Project**

## 1️⃣ **Run Machine Learning Service (Flask API)**

```
cd attendance/ml
pip install -r requirements.txt
python encode_faces.py
python app.py
```

Runs on:
👉 [http://127.0.0.1:5000/detect](http://127.0.0.1:5000/detect)

---

## 2️⃣ **Run Backend (Node.js + MongoDB)**

```
cd attendance/backend
npm install
```

Add `.env`:

```
MONGO_URI=mongodb://localhost:27017/attendance
PORT=8000
```

Start server:

```
node src/server.js
```

Backend:
👉 [http://localhost:8000/attendance](http://localhost:8000/attendance)

---

## 3️⃣ **Run Frontend (React Dashboard)**

```
cd attendance/fronted
npm install
npm start
```

Runs on:
👉 [http://localhost:3000](http://localhost:3000)

---

# 🔗 **API Endpoints**

### **ML Service**

| Method | Endpoint  | Description                 |
| ------ | --------- | --------------------------- |
| GET    | `/detect` | Detects face & returns JSON |

### **Backend API**

| Method | Endpoint      | Description          |
| ------ | ------------- | -------------------- |
| POST   | `/attendance` | Save attendance      |
| GET    | `/attendance` | Fetch all attendance |

---

# 🏆 **Author**

**Alok Ranjan**
Smart Attendance System — AI + ML + MERN + DevOps
(Feel free to connect or fork the repo!)

---
