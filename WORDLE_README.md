# 🎮 WORDLE - Python Edition

A command-line implementation of the popular word-guessing game WORDLE, built with Python. Test your vocabulary and deduction skills by guessing a 4-letter word in 5 attempts!

## 📋 Table of Contents
- [Overview](#overview)
- [Game Rules](#game-rules)
- [Features](#features)
- [Installation](#installation)
- [How to Play](#how-to-play)
- [Project Structure](#project-structure)
- [Game Logic](#game-logic)
- [Screenshots](#screenshots)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

## 🔍 Overview

This is a Python-based recreation of the popular WORDLE game. Players have 5 attempts to guess a randomly selected 4-letter word. After each guess, the game provides color-coded feedback to help narrow down the correct answer.

## 🎯 Game Rules

The game follows these simple rules:

1. **Objective**: Guess the target 4-letter word in 5 attempts or less
2. **Valid Guesses**: Only 4-letter words from the dictionary are accepted
3. **Feedback System**:
   - 🟦 **GREY**: Letter is not present in the target word
   - 🟨 **YELLOW**: Letter is in the word but in the wrong position
   - 🟩 **GREEN**: Letter is in the correct position

## ✨ Features

- 🎲 **Random Word Selection**: Each game selects a different word from a curated list
- ✅ **Input Validation**: Ensures players enter valid 4-letter words
- 🎨 **Color-Coded Feedback**: Clear visual hints after each guess
- 📊 **Attempt Tracking**: Shows remaining attempts after each guess
- 🏆 **Win/Loss Conditions**: Celebrates victories and reveals the answer on loss
- 💡 **User-Friendly Interface**: Clear instructions and intuitive gameplay

## 🚀 Installation

### Prerequisites
- Python 3.6 or higher
- `four_letter_words.py` module (contains the word list)

### Setup

1. **Clone the repository**:
```bash
git clone https://github.com/yourusername/wordle-python.git
cd wordle-python
```

2. **Ensure you have the word list file**:
Create a file named `four_letter_words.py` with the following structure:
```python
words = [
    "word", "play", "game", "they", "seen",
    "test", "code", "life", "time", "work",
    # Add more 4-letter words here
]
```

3. **Run the game**:
```bash
python WORDLE__.ipynb
```

Or use Jupyter Notebook:
```bash
jupyter notebook WORDLE__.ipynb
```

## 🎮 How to Play

1. **Start the Game**: Run the notebook cell to begin
2. **Read Instructions**: The game displays the rules and color-coding system
3. **Make Your Guess**: Enter a 4-letter word when prompted
4. **Review Feedback**: Check the color codes for each letter:
   - GREY: Not in the word
   - YELLOW: In the word, wrong spot
   - GREEN: Correct position
5. **Refine Your Strategy**: Use the feedback to make better guesses
6. **Win or Learn**: Guess the word within 5 attempts to win!

### Example Gameplay

```
Welcome to WORDLE!
GOAL: To find the target word in 5 attempts

Enter your guess (5 attempts remaining): seen
Guess 1 : seen - ['GREY', 'YELLOW', 'GREEN', 'GREY']

Enter your guess (4 attempts remaining): feel
Guess 2 : feel - ['GREY', 'YELLOW', 'GREEN', 'GREY']

Enter your guess (3 attempts remaining): they
Guess 3 : they - ['GREEN', 'GREEN', 'GREEN', 'GREEN']
CONGRATS! You found the target word in 3 guesses!
```

## 📁 Project Structure

```
wordle-python/
│
├── WORDLE__.ipynb              # Main game notebook
├── four_letter_words.py        # Word list module
├── README.md                   # Project documentation
└── requirements.txt            # Python dependencies (if any)
```

## 🧠 Game Logic

### Core Algorithm

```python
1. Select random word from dictionary
2. Initialize attempts counter (5)
3. For each guess:
   a. Validate input (length = 4, word in dictionary)
   b. Compare each letter with target:
      - Same position → GREEN
      - In word, wrong position → YELLOW
      - Not in word → GREY
   c. Display feedback
   d. Check win condition
4. End game (win or reveal answer)
```

### Key Functions

**Letter Checking Logic**:
```python
for i in range(4):
    if guess[i] == target[i]:
        feedback.append("GREEN")      # Correct position
    elif guess[i] in target:
        feedback.append("YELLOW")     # Wrong position
    else:
        feedback.append("GREY")       # Not in word
```

## 📸 Screenshots

### Game Start
```
Welcome to WORDLE!
GOAL: To find the target word in 5 attempts
Instructions:
(1) GREY, if letter is not present in the target word
(2) YELLOW, if letter is present in the word but not in the right spot
(3) GREEN, if letter is present at the correct position of the target word
(4) Enter 4 letter words ONLY
```

### During Gameplay
```
Guess 1 : seen - ['GREY', 'YELLOW', 'GREEN', 'GREY']
Guess 2 : feel - ['GREY', 'YELLOW', 'GREEN', 'GREY']
```

## 🔮 Future Enhancements

- [ ] **GUI Interface**: Create a graphical version with actual color blocks
- [ ] **5-Letter Words**: Add support for traditional 5-letter Wordle
- [ ] **Difficulty Levels**: Easy (4-letter), Medium (5-letter), Hard (6-letter)
- [ ] **Statistics Tracking**: Win rate, average attempts, streak counter
- [ ] **Daily Challenge**: Same word for all players each day
- [ ] **Hard Mode**: Used letters must be included in subsequent guesses
- [ ] **Hint System**: Optional hints for stuck players
- [ ] **Word of the Day**: Predetermined word rotation
- [ ] **Multiplayer Mode**: Compete with friends
- [ ] **Color Blind Mode**: Alternative symbols instead of colors
- [ ] **Save/Load Progress**: Continue games later

## 🛠️ Customization

### Adding More Words

Edit `four_letter_words.py` to expand the word list:
```python
words = [
    "your", "word", "list", "here",
    "make", "sure", "they", "exist",
    # Add as many as you want!
]
```

### Changing Difficulty

Modify the `attempts` variable in the code:
```python
attempts = 5  # Change to 3 (hard) or 7 (easy)
```

## 🎓 Learning Outcomes

This project demonstrates:
- **Control Flow**: Loops and conditionals
- **Data Structures**: Lists and strings
- **User Input**: Interactive command-line interface
- **Random Selection**: Using Python's `random` module
- **Input Validation**: Error handling and data validation
- **Game Logic**: Implementing rules and win conditions

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the project
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Ideas
- Add more words to the dictionary
- Create a GUI version
- Implement statistics tracking
- Add unit tests
- Improve input validation
- Create themed word lists (animals, countries, etc.)

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👏 Acknowledgments

- Inspired by the original [WORDLE](https://www.nytimes.com/games/wordle/index.html) by Josh Wardle
- Python community for excellent documentation
- All contributors and players!

## 📧 Contact

Your Name - [@yourhandle](https://twitter.com/yourhandle)

Project Link: [https://github.com/yourusername/wordle-python](https://github.com/yourusername/wordle-python)

---

**Happy Word Guessing! 🎉**

*Note: This is an educational project and is not affiliated with the official WORDLE game.*
