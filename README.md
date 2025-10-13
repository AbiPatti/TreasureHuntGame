# Cars Matching Game
### Abinash Patti

## Project Overview

The Cars Matching Game is a memory based tile game where the player has to uncover pairs of matching car images from Pixar's *Cars* Universe. The game challenges the player to test their memory as they race against the clock to find all matching players as quickly as they can.

**NOTE**: This project was develpoed as part of a school assignment. Due to the institution's academic integrity rules, the source code cannot be publicly shared. However, the project's explanation in this README and the video demo are provided to showcase how the project functions.

## Demonstration

## Game Logic

### Game State Variables
`mysteryTilesDictionary` – Maps each tile button’s ID to its hidden image name

`tileButton1, tileButton2` – Track the two tiles selected by the user

`TreasureTilesList` – Stores successfully matched images

`GameStartTime` – Records when the game started for timing purposes

### Game Initialization (`ReloadGame`)
**Image List Setup**: Four car images are added and duplicated to make pairs (total of eight)

**Tile Assignment**: Each button is assigned a random image; duplicates are avoided

**UI Reset**: All mystery tiles show a question mark, and treasure tiles display a magnifying glass

**State Reset**: Clears prior matches and resets selection variables

**Timer**: Begins tracking elapsed time for gameplay performance

### Tile Selection (`TileButton_OnClicked`)
**First Selection:**
Stored as tileButton1, image revealed, button disabled.

**Second Selection:**
Stored as tileButton2, image revealed, button disabled.
Matching logic is triggered once both are selected.

### Matching Logic
**If Match Found**:
Displays a success message
Adds the image to the treasure list
Updates treasure tile to show the found image
Replaces both matched tiles with a smiley face
If all pairs are found, displays an alert as congratulations and switches to the reward view

**If Not a Match:**
Displays an alert as failure
Resets both tiles to question marks and re-enables them
Clears selected tile variables for the next round

### Timer (`TimeUpdate`)
Continuously updates the timer label with elapsed seconds
Stops if all matches are found or if the player leaves the game view

### Other UI Events
**Play Again:** Resets the game board and returns to the main screen.
**Exit:** Closes the application cleanly.

## Technologies
**Framework:** .NET MAUI
**Languages:** C#, XAML
**IDE**: Visual Studio 2022

## Additional Notes
The purpose of this project was to practice and demonstrate core concepts in:

- Object-oriented programming (OOP)
- UI event handling
- State management
- Randomization and user interaction

## Future Improvements
- Difficulty levels (More tiles, lime limits)
- Animations and/or sound effects triggered by events
- Saved scores
