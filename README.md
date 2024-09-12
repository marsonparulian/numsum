# NumSum

**NumSum** is a simple, number-based addition game designed to help users practice basic math skills in a fun and engaging way. Inspired by the classic "Number Sum" game, this version offers a more gradual increase in difficulty, making it suitable for younger players and anyone looking to improve their addition speed.

## Motivation
I developed NumSum after noticing that the original "Number Sum" game could be too challenging for younger players, such as my 6-year-old son. The steep difficulty curve made the game less enjoyable and hindered its educational potential. By introducing adjustable difficulty levels, NumSum aims to provide a smoother learning experience that adapts to the user's skill level, making it a valuable tool for practicing basic addition skills.

## Target Audience
NumSum is perfect for anyone who wants to practice or improve their basic addition skills. While the game is primarily designed for children aged 5-12, it can also be useful for individuals of any age who want to improve their mental math speed and accuracy.

## Technologies
NumSum is built using the following technologies:
- **JavaScript** for game logic
- **Canvas API** for rendering game elements
- **HTML and CSS** for the user interface

## Gameplay Overview
Upon starting the game, the following steps occur:
1. The game engine retrieves saved data from the user's settings, including the current **Challenge Level**, which reflects the difficulty of the current game.
2. Based on the Challenge Level, the game generates a grid and populates it with random numbers.
3. The game engine draws the grid and numbers on the screen using the Canvas API, along with other visual elements.
4. The player must identify whether the displayed numbers are valid sums or incorrect (fake) values.
5. The player is given 5 attempts to make a mistake before the game ends.
6. After each game, the difficulty level adjusts based on the player's performance and the **Difficulty Acceleration Rate**, which can be set in the settings.

## Features
- **Adjustable Difficulty**: Players can control how quickly the difficulty increases, ensuring the game remains challenging yet manageable.
- **Progress Tracking**: The game saves the player's progress and adjusts the difficulty based on the current Challenge Level.
- **Engaging Visuals**: The grid and game elements are dynamically rendered using the Canvas API for smooth gameplay.
