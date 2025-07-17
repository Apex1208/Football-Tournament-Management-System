⚽ Football Tournament Management System
A comprehensive platform for organizing football tournaments, managing teams and fixtures, tracking live standings, predicting outcomes, and generating video highlights using audio/video processing.

🚀 Features
🏆 Tournament Management
Team registration and management
Fixture generation (round-robin or custom)
Result input interface

📊 Live Standings
Automatically updates based on match outcomes
Tracks wins, losses, draws, goals scored/conceded

🔮 Match Predictor
Predicts outcomes using pre-trained ML models (UCL, La Liga)
Dynamically supports user-generated tournaments

🎥 Highlight Generator
Extracts highlights from full match videos
Uses separate audio_processing and video_processing modules
Outputs trimmed highlight reels based on exciting moments

🛠️ Tech Stack
Backend: Python (Flask)
Frontend: HTML, CSS, JavaScript (Flask templating)
Database: SQLite (via Flask-SQLAlchemy)
Machine Learning: Scikit-learn, Pandas, NumPy
Highlight Generation: OpenCV, Librosa, MoviePy

🗂️ Project Structure
Football-Tournament-Management-System/
│
├── app/
│   ├── highlight_generator/
│   │   ├── audio_processing/
│   │   ├── video_processing/
│   │   ├── process_highlights.py
│   │   └── requirements.txt
│   ├── predictors/
│   ├── static/
│   ├── templates/
│   ├── models.py
│   └── routes.py
│
├── instance/
├── migrations/
├── .gitignore
└── README.md

⚙️ Setup Instructions
🔽 1. Clone the Repository
git clone https://github.com/Apex1208/Football-Tournament-Management-System.git
cd Football-Tournament-Management-System

🐍 2. Create a Virtual Environment (Recommended)
python -m venv venv
source venv/bin/activate       # On Linux/macOS
venv\Scripts\activate          # On Windows

📦 3. Install Required Dependencies
pip install -r requirements.txt
To install highlight-specific dependencies:
cd app/highlight_generator
pip install -r requirements.txt

🛢️ 4. Set Up the Database (Flask Migrate)
flask db init
flask db migrate -m "Initial migration"
flask db upgrade

▶️ 5. Run the Application
flask run
The app will start at: http://127.0.0.1:5000

🎥 How to Use the Highlight Generator
Input
Full match video (MP4)

Output
Trimmed highlight video containing the most exciting moments

Run Highlight Generation
cd app/highlight_generator
python process_highlights.py --input path/to/full_match.mp4 --output path/to/highlights.mp4

You can customize threshold values and detection strategy inside process_highlights.py.

📌 Future Enhancements
Admin dashboard for full control over leagues and teams
Real-time commentary using NLP
Live YouTube integration for auto-publishing highlights
Deep learning-based highlight detection (YOLO, etc.)

🤝 Project by
Bharath Nayakanti and Sagar Das

📄 License
This project is licensed under the MIT License. See LICENSE for more details.


