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
* 🐳 **Containerized with Docker** (future phase)
* ☸️ **Deployable on Kubernetes** (future phase)
* 🔄 **CI/CD using GitHub Actions** (future phase)

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

### Step 1 — Go to ML folder

```
cd attendance/ml
```

### Step 2 — Install dependencies

```
pip install -r requirements.txt
```

### Step 3 — Encode faces

```
python encode_faces.py
```

### Step 4 — Start ML server

```
python app.py
```

Flask will start on:

👉 [http://127.0.0.1:5000/detect](http://127.0.0.1:5000/detect)

---

## 2️⃣ **Run Backend (Node.js + MongoDB)**

### Step 1 — Go to backend folder

```
cd attendance/backend
```

### Step 2 — Install dependencies

```
npm install
```

### Step 3 — Add `.env`

```
MONGO_URI=mongodb://localhost:27017/attendance
PORT=8000
```

### Step 4 — Start backend

```
node src/server.js
```

Backend will start at:

👉 [http://localhost:8000/attendance](http://localhost:8000/attendance)

---

## 3️⃣ **Run Frontend (React Dashboard)**

### Step 1 — Go to frontend folder

```
cd attendance/fronted
```

### Step 2 — Install packages

```
npm install
```

### Step 3 — Start React app

```
npm start
```

Frontend will open at:

👉 [http://localhost:3000](http://localhost:3000)

You will see **live attendance updates** from MongoDB.

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

Just tell me!
