# Wordle – Python Implementation

## 📜 About
This is a Python implementation of the classic **Wordle** game.  
You have 6 tries to guess a secret 5-letter word.  
After each guess, you will receive feedback to help you get closer to the answer:
- **Green** → Letter is correct and in the right position.
- **Orange** → Letter is correct but in the wrong position.
- **Gray** → Letter is not in the word.

This project was created for **Task 6: Encrypted Message** as part of the assignment requirements.

---

## 🗂 Folder Structure
wordle_project/
│
├── main.py # Entry point of the game
├── README.md # Documentation
├── data/
│ └── words.txt # Dataset of valid 5-letter words
├── logic/
│ ├── word_selector.py # Handles loading and selecting words
│ ├── validator.py # Checks if a guess is valid
│ ├── feedback.py # Generates feedback for a guess
└── interface/
└── console_ui.py # Console-based user interface

---

## 🔄 Game Flow
1. Load all valid 5-letter words from the dataset.
2. Pick one word at random as the **secret word**.
3. Display an empty 5×6 grid.
4. User inputs a guess:
   - If it’s not a valid word → show error.
   - If valid → compare with secret word and give feedback.
5. Repeat until:
   - The user guesses the correct word (**Win**), or
   - The user uses all 6 attempts (**Lose**).

---

## ▶️ How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/wordle-python.git
   cd wordle-python
Enter your guess: apple
🟩⬜🟨⬜⬜
🟩 = Green (correct letter & position)

🟨 = Orange (correct letter, wrong position)

⬜ = Gray (letter not in word)
