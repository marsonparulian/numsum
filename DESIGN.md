# NUMSUM Design

**NumSum** is a modern take on the classic Number Sum game, featuring adjustable Challenge Levels (difficulty levels) and a visually appealing experience tailored for kids.

## Technology

### Platform
NumSum will be developed as a Progressive Web Application (PWA), allowing it to be installed and played offline.

### Scripting
- **JavaScript** will handle the game logic.
- **Canvas API** will be used for rendering the grid, cells, and numbers.
- **HTML** and **CSS** will be used for layout, text, links, and buttons.

### Data Storage
- **IndexedDB** will store user settings and game data.
- **Service Workers** will manage and cache game assets for offline play.

## Visual Design

The visual style of NumSum will be inspired by the Bootstrap library, sourced from a CDN, for a clean and consistent look.

### Top Bar
The top bar will appear on every screen and will include:
1. A small "NumSum" logo on the left.
2. A settings button and user name on the right. Clicking the settings button will display a "Settings" pop-up modal.

### Settings Pop-up Dialog
The settings modal will store data in IndexedDB and will include:
1. **Username**: An input field with a minimum of 2 characters and a maximum of 24 characters. An error message "invalid input" will appear in red below the input if the input is invalid.
2. **Challenge Level**: A range input from 1 to 100 to set the difficulty of the game.
3. **Challenge Increase Rate**: A range input from 1 to 100 with a step of 10 to control how quickly the challenge increases.
4. **OK Button**: Saves the user settings to IndexedDB and closes the settings modal.

### Home Screen
The home screen will be loaded from `index.html` and will feature:
- A large "NumSum" logo centered on the screen.
- Below it, a smaller text reading "Fun number game."
- A "Continue" button that navigates to the Game Screen.

### Game Screen
The game screen will be loaded from `/play.html` and will include:
1. **Erase/Keep Button**: A toggle button at the bottom with two options: "Erase" and "Keep." The button height will be approximately 20 pixels.
2. **Grid Area**: A grid of squares where each cell contains a number. The grid will include:
   - A row at the top displaying the sum of each column.
   - A column on the left showing the sum of each row.
   - The grid will occupy the remaining space on the screen.
3. **Lives Display**: Shows the total number of lives the player has. Remaining lives are displayed as full red heart icons, while lost lives are represented by open heart shapes. The height of the icons is 28px.

## Gameplay Overview
When starting a game, the following steps will occur:
1. The game engine retrieves saved data from IndexedDB, including the current **Challenge Level**, which determines the difficulty.
2. Based on the Challenge Level, the game generates a grid and fills it with random numbers.
3. The game engine uses the Canvas API to render the grid, numbers, and other visual elements on the screen.
4. The player must decide whether to "Erase" or "Keep" each number by selecting it. The action is determined by the state of the **Erase/Keep** switch button. Incorrect guesses will reduce the player's lives by 1, and the selected number will briefly shake and turn red for 1 second.
5. The player has 5 attempts to make a mistake before the game ends.
6. If the player correctly guesses all numbers, the `gameWon` function will be executed, displaying an animation to celebrate the victory.
7. After each game, the difficulty level will adjust based on the player's performance and the **Challenge Increase Rate** set in the settings.

## Installation
NumSum is a Progressive Web Application (PWA). You can install it directly from your web browser:

1. Visit the game's URL.
2. Click the "Install" or "Add to Home Screen" option in your browser.
3. Enjoy offline gameplay!

## Future Enhancements
- Additional gameplay modes for varied challenges.
- A leaderboard to track high scores.
- Improved animations and sound effects for a more engaging experience.

## License
NumSum is released under the MIT License. See LICENSE for more information.
