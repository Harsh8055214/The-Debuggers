# The-Debuggers
# Tetris Game

## Description
This is a simple console-based Tetris game implemented in C++. The game features a basic Tetris gameplay where players can move, rotate, and drop tetromino pieces to form and clear lines. The game keeps track of the player's score and allows restarting or quitting at any time.

## Features
- Seven different tetromino shapes (I, O, T, S, Z, J, L)
- Ability to move, rotate, and drop pieces
- Line clearing and scoring system
- Simple UI with ASCII graphics
- Keyboard controls for movement and game management
- Pause and resume functionality
- Game over detection

## Controls
- **Arrow Left (←):** Move the piece left
- **Arrow Right (→):** Move the piece right
- **Arrow Down (↓):** Move the piece down faster
- **Arrow Up (↑):** Rotate the piece
- **Spacebar:** Instantly drop the piece
- **P:** Pause/Resume the game
- **R:** Restart the game
- **Q:** Quit the game

## Compilation and Execution
### Windows
This game uses Windows-specific libraries (`conio.h`, `windows.h`), so it is intended to run on Windows.

#### Compile using g++ (MinGW):
```sh
 g++ tetris.cpp -o tetris.exe
```

#### Run the game:
```sh
 tetris.exe
```

## How to Play
1. The game starts automatically with a random tetromino at the top of the board.
2. Use arrow keys to move and rotate the piece.
3. Complete horizontal lines to clear them and earn points.
4. The game ends when pieces stack up to the top of the board.
5. Press 'R' to restart or 'Q' to quit.

## Functionality Overview
### `draw()`
Displays the game board, current piece, score, and controls on the console.

### `update()`
Moves the current piece down at a fixed interval. If the piece cannot move further, it locks the piece in place and generates a new one.

### `handleInput()`
Handles keyboard inputs to move, rotate, or drop the piece. Also allows pausing, quitting, and restarting the game.

### `canMove(int newX, int newY)`
Checks if the current piece can move to the specified position without colliding with existing blocks or the board boundaries.

### `lockPiece()`
Locks the current piece in place on the board and clears completed lines if necessary.

### `clearLines()`
Removes full rows from the board and shifts the remaining blocks down. Increases the score for each cleared line.

### `createNewPiece()`
Generates a new random tetromino. If the new piece cannot be placed, the game ends.

### `rotate()`
Rotates the current piece 90 degrees clockwise if there is space for it.

### `gameOver()`
Displays a game-over message and prompts the player to restart or quit.

### `run()`
The main game loop that continuously updates and renders the game while checking for user input.

## Future Improvements
- Add a preview of the next tetromino
- Implement a scoring system based on Tetris rules (e.g., combos and T-spins)
- Add a hold feature for swapping pieces
- Improve UI with better graphics

## Group Members
- Member 1 Name:- Thakor Bhavin ID:- 202401113
- Member 2 Name:- Kodavala Harshkumar ID:- 202401121
- Member 3 Name:- Panchal Harsh ID:- 202401134

## License
This project is open-source. Feel free to modify and distribute it!

