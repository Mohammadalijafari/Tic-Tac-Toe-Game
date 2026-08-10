Tic-Tac-Toe Game

A simple interactive Tic-Tac-Toe game built with React. The project provides a playable 3×3 game board, editable player names, turn tracking, move history, win detection, draw handling, and a rematch option.

Features

🎮 Interactive 3×3 Tic-Tac-Toe board

👥 Two-player gameplay

✏️ Edit player names during the game

🔄 Tracks the active player

📝 Displays a history of moves

🏆 Detects winning combinations

🤝 Detects draws

🔁 Restart/rematch functionality

⚛️ Built with React functional components and hooks

Project Structure

src/
├── GameBoard.jsx
├── GameOver.jsx
├── Log.jsx
├── Player.jsx
└── wining-combinations.jsx

Components

GameBoard.jsx

Renders the game board from a two-dimensional board array. Each square is represented by a button and becomes disabled after a symbol has been placed on it.

The component receives:

board — the current board state

onSelectSquare — callback invoked when a player selects a square

The square selection passes the row and column indexes to the parent component.

Player.jsx

Handles player information and editing.

Each player has:

A name

A symbol

An active/inactive state

An edit/save control

Player names are managed with React's useState hook and changes are passed back through the onChangeName callback.

Log.jsx

Displays the history of moves. Each turn records:

The player who made the move

The selected row

The selected column

GameOver.jsx

Displays the end-game state:

The winning player when there is a winner

A draw message when there is no winner

A Rematch button to restart the game

wining-combinations.jsx

Contains the winning combinations for the 3×3 board:

Three horizontal rows

Three vertical columns

Two diagonals

Note: The filename wining-combinations.jsx is kept as provided by the project. If you intend to rename it, update all imports accordingly.

How the Game Works

Two players participate using different symbols.

The active player selects an empty square.

The selected square is updated with the player's symbol.

The move is added to the game log.

The game checks the board against the predefined winning combinations.

If a player completes a winning combination, the game displays the winner.

If the board is full without a winner, the game is declared a draw.

Players can start another round using the Rematch button.

Winning Conditions

A player wins when their symbol occupies any complete row, column, or diagonal.

[ X ][ X ][ X ]    Row
[   ][   ][   ]

[ X ][   ][   ]    Column
[ X ][   ][   ]
[ X ][   ][   ]

[ X ][   ][   ]    Diagonal
[   ][ X ][   ]
[   ][   ][ X ]

React Concepts Used

This project demonstrates several core React concepts:

Functional components

Component props

State management with useState

Event handlers

Conditional rendering

Rendering lists with .map()

Controlled form inputs

Component composition

Installation

The uploaded project files contain the React components, but they do not include a package.json or project configuration file. Therefore, the exact package-manager commands and scripts cannot be verified from the supplied files.

If this project is part of a standard React/Vite application, the usual workflow is:

npm install
npm run dev

Use the commands defined in your project's package.json if they differ.

Usage

After starting the development server:

Open the application in your browser.

Enter or edit the player names if needed.

Select an empty square to make a move.

Continue taking turns until there is a winner or draw.

Select Rematch to play again.

Customization

The project can be extended with features such as:

Score tracking across multiple rounds

Player avatars

Responsive/mobile styling

Sound effects

Winning-square animations

AI/computer opponent

Difficulty levels

Persistent game history

Local storage support

Known Project Detail

The supplied component files use the identifier WINING_COMBINATIONS and the filename wining-combinations.jsx. The implementation contains the standard eight winning patterns for a 3×3 Tic-Tac-Toe board.

Author

Mohammadali Jafari

https://github.com/Mohammadalijafari