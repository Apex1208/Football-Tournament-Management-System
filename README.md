⚽ Football Tournament Management System<br/>
A comprehensive platform for organizing football tournaments, managing teams and fixtures, tracking live standings, predicting outcomes, and generating video highlights using audio/video processing.

🚀 Features<br/>
🏆 Tournament Management<br/>
Team registration and management<br/>
Fixture generation (round-robin or custom)<br/>
Result input interface<br/>

📊 Live Standings<br/>
Automatically updates based on match outcomes<br/>
Tracks wins, losses, draws, goals scored/conceded<br/>

🔮 Match Predictor<br/>
Predicts outcomes using pre-trained ML models (UCL, La Liga)<br/>
Dynamically supports user-generated tournaments<br/>

🎥 Highlight Generator<br/>
Extracts highlights from full match videos<br/>
Uses separate audio_processing and video_processing modules<br/>
Outputs trimmed highlight reels based on exciting moments<br/>

🛠️ Tech Stack<br/>
Backend: Python (Flask)<br/>
Frontend: HTML, CSS, JavaScript (Flask templating)<br/>
Database: SQLite (via Flask-SQLAlchemy)<br/>
Machine Learning: Scikit-learn, Pandas, NumPy<br/>
Highlight Generation: OpenCV, Librosa, MoviePy<br/>

🗂️ Project Structure<br/>
Football-Tournament-Management-System/<br/>
│<br/>
├── app/<br/>
│   ├── highlight_generator/<br/>
│   │   ├── audio_processing/<br/>
│   │   ├── video_processing/<br/>
│   │   ├── process_highlights.py<br/>
│   │   └── requirements.txt<br/>
│   ├── predictors/<br/>
│   ├── static/<br/>
│   ├── templates/<br/>
│   ├── models.py<br/>
│   └── routes.py<br/>
│
├── instance/<br/>
├── migrations/<br/>
├── .gitignore<br/>
└── README.md<br/>

⚙️ Setup Instructions<br/>
🔽 1. Clone the Repository<br/>
git clone https://github.com/Apex1208/Football-Tournament-Management-System.git<br/>
cd Football-Tournament-Management-System<br/>

🐍 2. Create a Virtual Environment (Recommended)<br/>
python -m venv venv<br/>
source venv/bin/activate       # On Linux/macOS<br/>
venv\Scripts\activate          # On Windows<br/>

📦 3. Install Required Dependencies<br/>
pip install -r requirements.txt<br/>
To install highlight-specific dependencies:<br/>
cd app/highlight_generator<br/>
pip install -r requirements.txt<br/>

🛢️ 4. Set Up the Database (Flask Migrate)<br/>
flask db init<br/>
flask db migrate -m "Initial migration"<br/>
flask db upgrade<br/>

▶️ 5. Run the Application<br/>
flask run<br/>
The app will start at: http://127.0.0.1:5000<br/>

🎥 How to Use the Highlight Generator<br/>
Input<br/>
Full match video (MP4)<br/>

Output<br/>
Trimmed highlight video containing the most exciting moments<br/>

Run Highlight Generation<br/>
cd app/highlight_generator<br/>
python process_highlights.py --input path/to/full_match.mp4 --output path/to/highlights.mp4<br/>

You can customize threshold values and detection strategy inside process_highlights.py.<br/>

📌 Future Enhancements<br/>
Admin dashboard for full control over leagues and teams<br/>
Real-time commentary using NLP<br/>
Live YouTube integration for auto-publishing highlights<br/>
Deep learning-based highlight detection (YOLO, etc.)<br/>

🤝 Project by<br/>
Bharath Nayakanti and Sagar Das<br/>

📄 License<br/>
This project is licensed under the MIT License. See LICENSE for more details.


