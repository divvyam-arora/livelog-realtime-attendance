# LiveLog - Smart Attendance System (Face Recognition)

A Python Flask-based smart attendance system using face recognition. This project allows you to mark and view attendance using facial recognition, with all data and models managed locally. The app is now structured for easy deployment on [Vercel](https://vercel.com/) as a serverless Python function.

---

## Features
- Mark attendance using face recognition (OpenCV + scikit-learn)
- View daily attendance records
- Add new users with face data (local only)
- Simple web interface (Flask + HTML)

---

## Folder Structure
```
.
├── api/
│   ├── index.py                  # Main Flask app (entry point for Vercel)
│   ├── requirements.txt          # Python dependencies
│   ├── haarcascade_frontalface_default.xml  # Face detection model
│   ├── static/
│   │   └── face_recognition_model.pkl       # Trained face recognition model
│   ├── templates/
│   │   └── home.html             # Main HTML template
│   └── Attendance/
│       ├── Attendance-*.csv      # Attendance records
├── vercel.json                   # Vercel routing config
└── README.md                     # This file
```

---

## Deploying on Vercel

1. **Push this repo to GitHub.**
2. **Connect your repo to Vercel** ([vercel.com/import](https://vercel.com/import)).
3. Vercel will auto-detect the Python API in `api/index.py` and install dependencies from `api/requirements.txt`.
4. All routes are handled by the Flask app.

> **Note:**
> - **Webcam features (marking attendance, adding users) will NOT work on Vercel** because serverless functions cannot access hardware. Only attendance viewing and data management features will work online.

---

## Local Development

To use all features (including webcam):

1. Clone the repo:
   ```bash
   git clone <your-repo-url>
   cd livelog-realtime-attendance/Smart Attendance System
   ```
2. Install dependencies:
   ```bash
   pip install flask opencv-python numpy scikit-learn pandas joblib
   ```
3. Run the app:
   ```bash
   python app.py
   ```
4. Open [http://localhost:5000](http://localhost:5000) in your browser.

---

## Limitations
- Webcam access is only available when running locally.
- On Vercel, only web-based features (like viewing attendance) are available.
- For full functionality, run the app on your own machine or a traditional server.

---

## Contact
For questions or contributions, open an issue or pull request on GitHub!

