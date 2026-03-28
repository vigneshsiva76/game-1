# MindSpark — Number Guessing Game
### Level 1: Beginner | Cognifyz Internship Task 1

---

## 📌 Task Overview

**Task:** Develop a basic text-based game  
**Objective:** Implement a simple game using conditional statements for game logic  
**Level:** Beginner

---

## 🎮 Game Description

**MindSpark** is a browser-based number guessing game where the computer picks a secret number and the player must guess it within a limited number of attempts. The game uses conditional statements to evaluate each guess and guide the player toward the answer.

---

## ✅ How It Meets the Requirements

| Step | Requirement | Implementation |
|------|-------------|----------------|
| 1 | **Choose a game type** | Number Guessing Game — classic, logic-driven, text-based |
| 2 | **Define game rules and logic** | Player guesses 1–100; limited attempts by difficulty; score calculated on win |
| 3 | **Use conditional statements to manage game flow** | `if/else if/else` logic handles: correct guess → win, no attempts left → lose, too high/low/close → contextual feedback |
| 4 | **Test and debug the game for correctness** | Input validation (NaN, out-of-range), edge cases for last attempt, all game states tested |

---

## 🔀 Conditional Logic (Game Flow)

```javascript
if (val === secretNumber) {
  // WIN — show victory screen
} else if (remaining <= 0) {
  // LOSE — reveal secret number
} else if (val < secretNumber) {
  if (diff > 30)      // "Way too low!"
  else if (diff > 10) // "Too low — go higher!"
  else                // "So close — just a bit higher!"
} else {
  if (diff > 30)      // "Way too high!"
  else if (diff > 10) // "Too high — go lower!"
  else                // "So close — just a bit lower!"
}
```

---

## 🕹️ How to Play

1. Open `index.html` in any modern browser (no server needed)
2. Select a **difficulty** — Easy (10 tries), Medium (7 tries), Hard (5 tries)
3. Click **Start Game**
4. Type a number between 1 and 100 and press **GUESS** or hit Enter
5. Read the feedback and narrow down your guess
6. Win by finding the number before you run out of attempts!

---

## 📁 Project Structure

```
text_game/
├── index.html    ← Game UI, logic (HTML + JavaScript)
├── style.css     ← All visual styling and animations
└── README.md     ← This file
```

---

## 🛠️ Technologies Used

- **HTML5** — structure and game screens
- **CSS3** — custom properties, animations, responsive design
- **Vanilla JavaScript** — all game logic, conditional statements, DOM manipulation
- **Google Fonts** — Syne (display) + JetBrains Mono (data)

---

## 🏆 Scoring

| Attempts Used | Score |
|---------------|-------|
| 1             | 920   |
| 3             | 760   |
| 5             | 600   |
| 7             | 440   |
| 10            | 200   |

Score formula: `max(100, 1000 - attempts × 80)`

---

## 🐛 Debugging & Testing

The game handles the following edge cases:

- **Non-numeric input** → shake animation + warning message
- **Out-of-range numbers** → rejected with feedback
- **Last attempt warning** → "LAST CHANCE!" appended to feedback
- **All difficulty levels** → tested for correct attempt limits
- **Win/Lose screens** → correctly display the number and score

---

*Built for Cognifyz Internship — Level 1, Task 1*
