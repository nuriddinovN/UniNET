# 📌 Telegram Match Bot

A fun Telegram bot that registers students by collecting their contact details, faculty, year/course, and interests, then stores the data into a CSV file for future matching.

---

## 🎯 Purpose of the Bot
The purpose of this bot is to **connect students with similar interests and academic backgrounds**. By collecting user information such as faculty, course, and hobbies, the bot creates a database that can later be used to match students for study groups, projects, or just making new friends.

Think of it as a **student networking assistant** that helps you meet like-minded people in your university community! 🤝

---

## ⚙️ How It Works
1. A user starts the bot with `/start`.
2. The bot guides them step by step to:
   - Share phone number (via button or text)
   - Enter their full name
   - Choose their faculty 🎓
   - Enter their course/year 📚
   - Write about their interests and hobbies 💡
   - The bot also automatically collects their Telegram username.
3. All details are saved into a `registrations.csv` file.
4. At the end, the bot sends a confirmation message: *“✅ You’re all set! Sit tight — we’re finding your best match.”*
5. The stored data can later be processed to match students with similar profiles.

---

## 🚀 Features
- Collects:
  - Phone number
  - Name
  - Faculty
  - Year/course number
  - Interests and hobbies
  - Telegram username (auto)
- Saves all registration data into `registrations.csv`
- Fun, interactive Telegram-style messages with emojis 🎉
- Error handling for invalid inputs

---

## 🛠️ Requirements
- Python **3.8+**
- `pip` (Python package manager)

### Install Python & pip
#### Linux (Ubuntu/Debian):
```bash
sudo apt update
sudo apt install python3 python3-pip -y
```

#### Fedora:
```bash
sudo dnf install python3 python3-pip -y
```

#### macOS (with Homebrew):
```bash
brew install python3
```

#### Windows:
1. Download and install Python from [python.org](https://www.python.org/downloads/).
2. During installation, check **"Add Python to PATH"**.

---

## 📦 Setup Instructions

1. **Clone this repository**
```bash
git clone https://github.com/YOUR_USERNAME/telegram-match-bot.git
cd telegram-match-bot
```

2. **Create a virtual environment (recommended)**
```bash
python3 -m venv venv
source venv/bin/activate   # Linux/macOS
venv\Scripts\activate      # Windows
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

If `requirements.txt` is missing, install manually:
```bash
pip install python-telegram-bot
```

4. **Set up your bot token**
- Get a bot token from [@BotFather](https://t.me/BotFather) on Telegram.
- Replace the `BOT_TOKEN` value inside the script with your token.

---

## ▶️ Run the Bot
```bash
python telegram_match_bot_registration.py
```

The bot will start and run in polling mode.

---

## 📂 Output
- Registrations are saved to `registrations.csv` with the following fields:
  - `telegram_id`
  - `username`
  - `phone`
  - `name`
  - `faculty`
  - `course`
  - `interests`
  - `timestamp`

---

## 🛑 Stopping the Bot
- Press **CTRL+C** in the terminal.

---

## ⚠️ Notes
- **Do not share your bot token publicly**. If exposed, regenerate it via BotFather.
- For production, consider using **webhooks** instead of polling.
- For larger projects, migrate from CSV → SQLite/Postgres for safer storage.

---

## 👨‍💻 Author
Developed by [Your Name] — feel free to contribute and improve this fun matching bot! 🎓🤝
