# Flask Memory Game 🧠

A simple and interactive **Memory Game** built using **Flask**, HTML, CSS, and JavaScript. The objective is to find all matching pairs of cards with as few moves as possible.

## Features

* 🎴 Interactive memory card game
* 🔄 Cards can be flipped to reveal their symbols
* 🧩 Matching-pair detection
* 🔢 Move counter
* 🏆 Game completion detection
* 🔁 Restart/play-again functionality
* 📱 Responsive and user-friendly interface
* 🌐 Flask-based backend

## Tech Stack

* **Python 3**
* **Flask**
* **HTML5**
* **CSS3**
* **JavaScript**

## Project Structure

```text
flask-memory-game/
│
├── app.py                 # Flask application
├── requirements.txt       # Python dependencies
│
├── templates/
│   └── index.html         # Main game page
│
├── static/
│   ├── css/
│   │   └── style.css      # Game styling
│   └── js/
│       └── script.js      # Game logic
│
└── README.md              # Project documentation
```

## Getting Started

### 1. Clone the repository

```bash
git clone <repository-url>
cd flask-memory-game
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**Windows:**

```bash
venv\Scripts\activate
```

**macOS/Linux:**

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

If `requirements.txt` does not exist, install Flask directly:

```bash
pip install Flask
```

### 4. Run the application

```bash
python app.py
```

The application should start on the local Flask development server.

Open your browser and visit:

```text
http://127.0.0.1:5000/
```

## How to Play

1. Click on a card to reveal its symbol.
2. Click on another card to reveal the second symbol.
3. If the two cards match, they remain visible.
4. If they do not match, they are flipped back.
5. Continue until all pairs have been matched.
6. Try to complete the game using the fewest possible moves.

## Flask Application

The Flask backend is responsible for serving the game interface and static assets. The main route typically looks like:

```python
from flask import Flask, render_template

app = Flask(__name__)

@app.route("/")
def home():
    return render_template("index.html")

if __name__ == "__main__":
    app.run(debug=True)
```

The majority of the game mechanics can be handled on the client side using JavaScript, while Flask provides the web application structure and serves the required files.

## Customization

You can extend the game by adding features such as:

* Difficulty levels
* Timer
* Best-score tracking
* Sound effects
* Animations
* Different card themes
* Player names
* Persistent high scores using a database
* User authentication
* Leaderboards

## Future Improvements

* Add multiple difficulty levels.
* Store scores in SQLite or another database.
* Add a countdown timer.
* Add accessibility improvements.
* Add multiplayer functionality.
* Deploy the game to a cloud hosting platform.

## License

This project is available for educational and personal use. Add an appropriate license file if you plan to distribute the project publicly.

## Author

Developed as a Flask-based web development project.
