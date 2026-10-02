# 🎓 SnapClass: AI Attendance System

A multi-modal attendance system that verifies students using **face recognition, voice recognition and QR codes**. Built with **Python and Streamlit**, with **Supabase** as the backend for users, classes and attendance records.

🔗 **Live Demo:** [snapclass-landing-page-tau.vercel.app](https://snapclass-landing-page-tau.vercel.app/)

<!--
Add screenshots here after uploading them to a /screenshots folder, e.g.:
![Landing page](screenshots/landing.png)
![Teacher dashboard](screenshots/teacher.png)
-->

---

## ✨ Features

- 🙂 **Face recognition** attendance using `dlib` and `face_recognition`
- 🎙️ **Voice verification** using Resemblyzer speaker embeddings
- 📱 **QR-based check-in** as an additional verification method
- 👩‍🏫 **Teacher and student roles** with separate views
- 🔑 **Class enrollment via unique join codes**
- ☁️ **Supabase backend** for data storage
- 🌐 **Deployed live** on Vercel

---

## 🛠️ Tech Stack

| Layer | Technologies |
|---|---|
| Language | Python |
| UI | Streamlit |
| Face recognition | dlib, face_recognition, OpenCV |
| Voice recognition | Resemblyzer |
| Database and auth | Supabase |
| Deployment | Vercel |

---

## 🧠 How It Works

1. **Teacher** creates a class and gets a unique join code.
2. **Students** enroll in the class using that code and register their face and voice.
3. During attendance, the student verifies with **face**, **voice**, or a **QR code**.
4. The result is saved to Supabase and the teacher can view attendance records.

---

## 📁 Project Structure

```
ai-attendance-system/
├── src/               # Application modules (face, voice, QR, database logic)
├── app.py             # Streamlit entry point
├── requirements.txt   # Python dependencies
└── .gitignore
```

---

## 🚀 Run It Locally

### Prerequisites
- Python 3.9 or higher
- A [Supabase](https://supabase.com/) project
- A webcam and microphone

> ⚠️ `dlib` needs CMake and a C++ compiler to build. On Windows, install **Visual Studio Build Tools**. On Ubuntu, run `sudo apt install cmake build-essential`.

### 1. Clone the repository
```bash
git clone https://github.com/KaranKumar7646/ai-attendance-system.git
cd ai-attendance-system
```

### 2. Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Add your Supabase credentials
Create a `.streamlit/secrets.toml` file (or a `.env` file, depending on how your code reads them):
```toml
SUPABASE_URL = "your_supabase_project_url"
SUPABASE_KEY = "your_supabase_anon_key"
```

### 5. Run the app
```bash
streamlit run app.py
```
Open **http://localhost:8501** in your browser.

---

## 🔮 Future Improvements

- Attendance reports and CSV export
- Liveness detection to prevent photo spoofing
- Email or SMS notifications for absences
- Mobile-friendly UI

---

## 👤 Author

**Karan Kumar**
[GitHub](https://github.com/KaranKumar7646) · [LinkedIn](https://www.linkedin.com/in/karan-kumar-687854282/)

⭐ If you found this project useful, consider giving it a star!
