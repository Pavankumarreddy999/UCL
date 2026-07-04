# 🏏 Ultimate Cricket League (UCL)

A full-featured **Cricket Tournament Management System** built with Django. UCL allows you to manage teams, players, matches, live scoring, standings, and player statistics — all from a single web application.

---

## 🚀 Features

- 🏟️ **Team Management** — Create and manage cricket teams with logos, home grounds, captains, and coaches
- 👤 **Player Management** — Register players with batting/bowling styles, roles, jersey numbers, and photos
- 📅 **Match Scheduling** — Schedule matches between teams with venue and toss details
- 📡 **Live Scoring** — Real-time ball-by-ball score updates with over tracking
- 📊 **Statistics** — Detailed batting and bowling stats (average, strike rate, economy rate, etc.)
- 🏆 **Standings** — Automatic points table based on match results
- 🔐 **User Authentication** — Register, login, and logout functionality
- 💬 **Messaging** — In-app messaging between users
- ⭐ **Favourites** — Bookmark your favourite teams and players

---

## 🛠️ Tech Stack

| Technology     | Version  |
|----------------|----------|
| Python         | 3.x      |
| Django         | 5.2.7    |
| Pillow         | 9.5.0    |
| python-dotenv  | 1.0.0    |
| SQLite         | (default)|

---

## 📁 Project Structure

```
UltimateCricketLeage/
└── UCL/
    ├── UCL/                  # Django project settings
    │   ├── settings.py
    │   ├── urls.py
    │   ├── asgi.py
    │   └── wsgi.py
    ├── tournament/           # Main app
    │   ├── models.py         # Team, Player, Match, Ball, etc.
    │   ├── views.py          # All view logic
    │   ├── urls.py           # URL routing
    │   ├── forms.py          # Django forms
    │   ├── admin.py          # Admin panel config
    │   ├── consumers.py      # WebSocket consumers
    │   ├── signals.py        # Django signals
    │   ├── templates/        # HTML templates
    │   └── static/           # CSS, JS, images
    ├── media/                # Uploaded files (logos, photos)
    ├── manage.py
    ├── db.sqlite3
    └── requirements.txt
```

---

## ⚙️ Setup & Installation

### Prerequisites
- Python 3.x installed
- Git (optional)

### Step 1 — Clone the Repository
```bash
git clone <your-repo-url>
cd UltimateCricketLeage/UCL
```

### Step 2 — Create a Virtual Environment
```bash
python -m venv venv
```

### Step 3 — Activate the Virtual Environment

**Windows (PowerShell):**
```powershell
.\venv\Scripts\Activate.ps1
```

**Windows (Command Prompt):**
```cmd
venv\Scripts\activate.bat
```

**Linux / macOS:**
```bash
source venv/bin/activate
```

> ✅ You will see `(venv)` at the start of your terminal prompt when activated.

### Step 4 — Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 5 — Apply Migrations
```bash
python manage.py migrate
```

### Step 6 — Create a Superuser (Admin)
```bash
python manage.py createsuperuser
```

### Step 7 — Run the Development Server
```bash
python manage.py runserver
```

Then open your browser and visit: **http://127.0.0.1:8000/**

---

## 🔗 Key URLs

| URL                        | Description                  |
|----------------------------|------------------------------|
| `/`                        | Landing page                 |
| `/index`                   | Home / Dashboard             |
| `/teams/`                  | List all teams               |
| `/players/`                | List all players             |
| `/matches/`                | List all matches             |
| `/standings/`              | Points table / Standings     |
| `/player_stats/`           | Player statistics            |
| `/accounts/register/`      | Register a new user          |
| `/login/`                  | Login page                   |
| `/admin/`                  | Django admin panel           |

---

## 🎮 Live Match Scoring

UCL supports live ball-by-ball score updates:

- Set a match as **Live** from the match detail page
- Record each ball: runs, extras (wide, no-ball, bye), wickets
- Track **current run rate (CRR)** and **required run rate (RRR)**
- Manage **powerplay** overs (first 6 overs)
- Start **second innings** and swap batting/bowling teams
- View real-time match data via `/match/<id>/live_data/`

---

## 📊 Data Models

| Model                | Description                                      |
|----------------------|--------------------------------------------------|
| `Team`               | Cricket team with stats (wins, losses, points)   |
| `Player`             | Player with batting and bowling stats            |
| `Match`              | Match details, scores, innings, and live data    |
| `BattingPerformance` | Per-match batting stats for each player          |
| `BowlingPerformance` | Per-match bowling stats for each player          |
| `Ball`               | Ball-by-ball record                              |
| `Message`            | In-app messaging between users                   |
| `Favorite`           | User favourite teams and players                 |

---

## 🛑 Deactivating the Virtual Environment

When you are done, deactivate the virtual environment:
```bash
deactivate
```

---

## 🤝 Contributing

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m "Add your feature"`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📄 License

This project is for educational purposes. Feel free to use and modify it.

---

> Built with Django | Ultimate Cricket League 2026
