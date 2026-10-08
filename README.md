# 💧 AquaPal Pro — Desktop Water Buddy

> **Stay hydrated. Stay focused. Let AquaPal remind you. 💦**

**AquaPal Pro** is a lightweight, intelligent desktop hydration assistant built with **Python and PyQt6**. It runs quietly in the background and helps users maintain healthy hydration habits through smart reminders, desktop widgets, system-tray controls, progress tracking, achievements, themes, and positive visual feedback.

Designed primarily for **Windows 10/11**, AquaPal Pro combines a simple desktop interface with useful system-level features to create an engaging hydration-tracking experience.

---

## ✨ Features

### 💧 Smart Hydration Reminders

* Customizable water reminder intervals.
* Desktop notification reminders.
* Automatic reminder scheduling.
* Pause and resume reminders whenever needed.
* Notifications automatically close after a defined timeout.

### 🕘 Smart Work Hours

AquaPal Pro can automatically manage reminders around your working schedule.

* Default work hours: **9:00 AM – 5:00 PM**
* Default working days: **Monday – Friday**
* Automatically pauses reminders outside working hours.
* Calculates the next reminder/resume time.
* Helps prevent unnecessary notifications during personal time.

### 📊 Daily Hydration Tracking

Track your daily water consumption with persistent local storage.

* Record water intake throughout the day.
* View daily hydration progress.
* Automatically reset daily statistics.
* Store tracking information locally using JSON.
* Quickly log water from multiple locations.

### 🏆 Achievement System

Stay motivated by unlocking hydration achievements.

Example achievements include:

* 💧 **First Drop** — Log your first glass of water.
* 🎯 **Goal Crusher** — Reach your daily hydration goal.
* 👑 **Hydration King** — Maintain consistent hydration progress.

The achievement system adds a simple gamification layer to encourage healthy habits.

### 🖥️ Desktop Widget

AquaPal Pro includes a lightweight desktop widget that provides quick access to hydration progress.

Features include:

* 📈 Real-time progress display.
* ➕ Quick water logging.
* 🖱️ Draggable widget.
* 🌫️ Semi-transparent desktop interface.
* 💧 Always-visible hydration status.

### ⚙️ System Tray Integration

AquaPal Pro can run quietly in the Windows system tray.

From the tray menu, users can:

* 💧 Log water.
* ⏸️ Pause reminders.
* ▶️ Resume reminders.
* ⚙️ Open settings.
* ❌ Exit the application.

This allows the application to remain active without occupying the desktop.

### 🎨 Custom Themes

Personalize the application using multiple visual themes:

* 🌑 Dark
* ☀️ Light
* 🌊 Ocean
* 💗 Pink

Each theme provides its own visual style and notification experience.

### 🤖 Custom Hydration Buddies

Choose a character to accompany your hydration journey.

Available characters can include:

* 👧 Girl
* 💧 Water Droplet
* 🐸 Frog
* 🤖 Robot

Characters can provide visual feedback during hydration events.

### 😊 Happy Reaction

AquaPal Pro provides positive feedback when water is logged.

After recording water intake:

* Character changes to a happy/celebratory image.
* Encouraging text is displayed.
* Optional sound feedback is played.

### 🎵 Notification Sounds

Different themes can use different notification sounds.

Supported audio formats include:

```text
.wav
```

If a custom sound is unavailable, the application can gracefully fall back to the Windows system notification sound.

### 🌅 Context-Aware Messages

AquaPal Pro changes messages depending on the current time of day.

Examples:

```text
🌅 Good Morning!
💧 Time to hydrate and start your day strong.

☀️ Good Afternoon!
💦 Don't forget to drink some water.

🌙 Good Evening!
💧 Keep yourself hydrated before finishing the day.
```

---

# 🛠️ Technology Stack

| Technology                   | Purpose                        |
| ---------------------------- | ------------------------------ |
| 🐍 Python 3.10+              | Core application development   |
| 🖼️ PyQt6                    | Desktop GUI                    |
| 🔊 PyQt6 Multimedia          | Audio playback                 |
| 💾 JSON                      | Local hydration data storage   |
| 🪟 Windows API / System Tray | Background desktop integration |
| 📦 PyInstaller               | Windows executable generation  |
| 💻 Windows 10/11             | Primary target platform        |

---

# 🏗️ Project Architecture

AquaPal Pro follows a lightweight desktop-application architecture:

```text
                    ┌─────────────────────┐
                    │     AquaPal Pro     │
                    │     Python App      │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
              ▼                ▼                ▼
       ┌─────────────┐  ┌─────────────┐  ┌─────────────┐
       │   PyQt6 UI  │  │  Reminder   │  │   Tracking  │
       │             │  │   Engine    │  │    System   │
       └──────┬──────┘  └──────┬──────┘  └──────┬──────┘
              │                │                │
              ▼                ▼                ▼
       ┌─────────────┐  ┌─────────────┐  ┌─────────────┐
       │   Widget    │  │ Notifications│ │ JSON Storage│
       └─────────────┘  └─────────────┘  └─────────────┘
              │
              ▼
       ┌─────────────┐
       │ System Tray │
       └─────────────┘
```

---

# 📁 Project Structure

```text
aquapal-pro/
│
├── aquapal_pro.py
│
├── character.png
├── character.gif
├── character_happy.png
│
├── sound_dark.wav
├── sound_light.wav
├── sound_ocean.wav
├── sound_pink.wav
│
├── hydration_data.json
├── requirements.txt
├── README.md
└── LICENSE
```

### File Description

| File                  | Description                        |
| --------------------- | ---------------------------------- |
| `aquapal_pro.py`      | Main application source code       |
| `character.png`       | Default character image            |
| `character.gif`       | Optional animated character        |
| `character_happy.png` | Happy/reaction character           |
| `sound_*.wav`         | Theme-specific notification sounds |
| `hydration_data.json` | Local hydration tracking data      |
| `requirements.txt`    | Python dependencies                |
| `README.md`           | Project documentation              |
| `LICENSE`             | Project license                    |

> ⚠️ `hydration_data.json` is generated/updated by the application and should generally not contain personal data when committing the project to GitHub.

---

# 🚀 Installation

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/chaitanyamodi-dev/aquapal-pro.git
```

Navigate into the project:

```bash
cd aquapal-pro
```

---

## 2️⃣ Create a Virtual Environment

### Windows

```bash
python -m venv venv
```

Activate it:

```bash
venv\Scripts\activate
```

---

## 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

Or install PyQt6 directly:

```bash
pip install PyQt6
```

---

## 4️⃣ Run AquaPal Pro

```bash
python aquapal_pro.py
```

The application should launch with the AquaPal Pro interface.

---

# 📦 Requirements

Create a `requirements.txt` file:

```txt
PyQt6>=6.6.0
```

For building the Windows executable:

```bash
pip install pyinstaller
```

---

# 🎮 How to Use

### Step 1 — Launch the Application

Start AquaPal Pro:

```bash
python aquapal_pro.py
```

---

### Step 2 — Configure Your Preferences

Choose:

* 💧 Reminder interval
* 🎨 Application theme
* 🤖 Hydration buddy
* 🕘 Smart Work Hours
* 🖥️ Desktop Widget

---

### Step 3 — Start AquaPal

Click:

```text
Start AquaPal
```

The application can then continue running in the background.

---

### Step 4 — Log Water

Water can be logged through multiple interfaces:

**Notification**

```text
✓ Drank It
```

**Desktop Widget**

```text
+ Log Water
```

**System Tray**

```text
Right Click → Log Water (+1)
```

---

### Step 5 — Track Your Progress

Your hydration progress is stored locally and can be updated throughout the day.

Example:

```text
Daily Goal: 2500 ml

██████████████░░░░░░ 70%

1750 / 2500 ml
```

---

# 🏆 Achievement Examples

| Achievement         | Requirement                       |
| ------------------- | --------------------------------- |
| 💧 First Drop       | Log your first water intake       |
| 🎯 Goal Crusher     | Reach your daily hydration goal   |
| 🔥 Hydration Streak | Maintain consistent hydration     |
| 👑 Hydration King   | Reach a major hydration milestone |

---

# 🖥️ Windows Executable

You can package AquaPal Pro as a standalone Windows executable using **PyInstaller**.

Install PyInstaller:

```bash
pip install pyinstaller
```

Build the application:

```bash
pyinstaller --noconsole --onefile aquapal_pro.py
```

The executable will be generated inside:

```text
dist/
└── aquapal_pro.exe
```

---

## 🎨 Building With an Application Icon

If you have an icon file:

```text
app_icon.ico
```

Run:

```bash
pyinstaller --noconsole --onefile --icon=app_icon.ico aquapal_pro.py
```

---

## ⚠️ Asset Deployment

If images and sound files are loaded externally, make sure they are available when distributing the application.

Example:

```text
dist/
├── aquapal_pro.exe
├── character.png
├── character_happy.png
├── sound_dark.wav
├── sound_light.wav
├── sound_ocean.wav
└── sound_pink.wav
```

For a production build, these assets can also be bundled directly into the executable using PyInstaller's `--add-data` configuration.

---

# 🔒 Data & Privacy

AquaPal Pro is designed as a local desktop application.

Hydration data is stored locally using:

```text
hydration_data.json
```

The application does not require a cloud account or external database for its core functionality.

---

# 💡 Why I Built AquaPal Pro

AquaPal Pro was created to solve a simple everyday problem:

> **People often forget to drink enough water while working for long periods.**

Instead of creating another complicated health application, the goal was to build a small desktop assistant that stays in the background and provides timely reminders without interrupting the user's workflow.

The project also provided an opportunity to work with:

* Python desktop development
* GUI design
* Event-driven programming
* Background processes
* System tray applications
* Local data persistence
* Multimedia handling
* Notification systems
* User experience design
* Application packaging

---

# 📸 Screenshots

Add screenshots of your application here.

### 🏠 Main Application

```text
Add screenshot here
```

### 💧 Hydration Notification

```text
Add screenshot here
```

### 🖥️ Desktop Widget

```text
Add screenshot here
```

### ⚙️ Settings

```text
Add screenshot here
```

### 🏆 Achievement System

```text
Add screenshot here
```

> 💡 Screenshots make the repository much more attractive to recruiters and other developers.

---

# 🔮 Future Improvements

Potential improvements for future versions include:

* [ ] ☁️ Cloud synchronization
* [ ] 📱 Mobile companion application
* [ ] 📊 Weekly and monthly hydration analytics
* [ ] 📈 Hydration history charts
* [ ] 🔔 Advanced notification customization
* [ ] 🌐 Multi-language support
* [ ] 👤 Multiple user profiles
* [ ] 🗄️ SQLite database support
* [ ] 🔐 User authentication
* [ ] 🏅 More achievements and streaks
* [ ] 🪟 Windows startup integration
* [ ] 📦 Improved PyInstaller packaging
* [ ] 🤖 AI-powered hydration recommendations

---

# 🤝 Contributing

Contributions, suggestions, and feature requests are welcome!

### 1. Fork the repository

```bash
git clone https://github.com/chaitanyamodi-dev/aquapal-pro.git
```

### 2. Create a feature branch

```bash
git checkout -b feature/amazing-feature
```

### 3. Commit your changes

```bash
git add .
git commit -m "Add amazing feature"
```

### 4. Push your branch

```bash
git push origin feature/amazing-feature
```

### 5. Open a Pull Request

Describe your changes and submit the pull request.

---

# 🐛 Bug Reports & Feature Requests

If you discover a bug or have an idea for improving AquaPal Pro, please create a GitHub Issue.

When reporting a bug, include:

* 🖥️ Windows version
* 🐍 Python version
* 📦 PyQt6 version
* 📝 Steps to reproduce
* 📸 Screenshot/error message if available

---

# 📄 License

This project is licensed under the **MIT License**.

See the [`LICENSE`](LICENSE) file for more information.

---

# 👨‍💻 Author

## Chaitanya Modi

**Python Backend Developer**

💼 InheritX Solutions

📧 `chaitanyamodi972004@gmail.com`

🔗 **LinkedIn:**
https://linkedin.com/in/chaitanya-modi-dev

🐙 **GitHub:**
https://github.com/chaitanyamodi-dev

---

# ⭐ Support the Project

If you find **AquaPal Pro** useful or interesting:

⭐ Star the repository
🍴 Fork the project
🐛 Report bugs
💡 Suggest features
🤝 Contribute improvements

---

<div align="center">

### 💧 Stay Hydrated. Stay Focused. Stay Healthy. 💧

**AquaPal Pro — Your Personal Desktop Hydration Buddy**

Made with ❤️ and Python 🐍

</div>
