# Centurion Game Prototype

A two-player “Centurion” arithmetic card game implemented in Python.

🚀 Getting Started

### Prerequisites

• Python 3.9+
• Git

### Installation

1. Clone the repo (FOLLOW THIS STEP ONE TIME ONLY)

```
git clone https://github.com/devguy101decka/centurion-game.git
cd centurion-game
```
### 1.1 After cloning - open The game folder (START FROM THIS STEP AFTER CLONING FOR THE FIRST TIME)
```
cd ~/centurion-game
```
2. Create & activate a virtual environment

In Git Bash you can use the py launcher:
```
py -3 -m venv .venv
```
(If py isn’t found, try python -m venv .venv.)

Activate the venv
```
source .venv/Scripts/activate
```

3. Install dependencies

```
pip install -r requirements.txt
```

🧪 Running the Test Suite

```
pytest -q
```

### 🎮 Playing the Game

GUI Interface

```
python run_game_tk.py
```

• Deals seven cards each; players take turns entering a card index to play.
• Running totals and deal outcomes appear in color:
– Red/White suits
– Cyan for current totals
– Green prompts
– Yellow victory messages


### 📚 How It Works

1. Deal Phase
   – Shuffle a 52-card deck (no Jokers by default)
   – Deal 7 cards each

2. Play Phase
   – Players alternate playing one card
   – Card value = rank × suit weight (Jokers = 0)
   – Running total updates each play

3. Deal-End Conditions
   – Total == 100 → end deal
   – Total > 100 and multiple of 10 → end deal
   – Either hand empties → end deal

4. Scoring
   – Base points = cards played
   – Penalty = [(total – 100)/10] (0 if total ≤ 100)
   – Final points = base – penalty
   – Deal winner takes that many counters

5. Match End
   – First to drain the shared 21-counter pool wins

### 🤝 Contributing

Feel free to open issues or pull requests to:

• Add new features (AI, networked play)
• Improve UI or test coverage

---

Built by Hadiqa 
