# Space Ship Battle Game

## Overview
This simple JavaScript game lets you pilot a spaceship and battle against an AI-controlled enemy ship. Your spaceship is controlled via the keyboard, and you can also modify the enemy AI using custom JavaScript code.

## How to Play

### Player Controls
- **Rotate Left:** Press the **Left Arrow** key.
- **Rotate Right:** Press the **Right Arrow** key.
- **Accelerate:** Press the **Up Arrow** key.
- **Shoot:** Press the **Spacebar** (200ms cooldown).

### Gameplay
- Your ship (displayed in **cyan**) is the player’s spaceship.
- The enemy ship (displayed in **red**) is controlled by an AI.
- Both ships can shoot bullets that reduce their opponent’s health.
- When a ship’s health reaches zero, it is destroyed and removed from the game.

## AI Customization

### Modifying Enemy Behavior
1. **Edit the AI Code:**  
   Use the text area provided in the game interface (associated with the `shipCode` element) to write or modify JavaScript code.

2. **Define the `runAI` Function:**  
   Your code must define a function named `runAI`. This function receives two parameters:
   - **aiShip:** The enemy ship object.
   - **aiApi:** An API object providing utility functions:
     - `aiApi.turnLeft(ship)`: Rotate the ship left.
     - `aiApi.turnRight(ship)`: Rotate the ship right.
     - `aiApi.thrust(ship)`: Accelerate the ship.
     - `aiApi.shoot(ship)`: Fire a bullet.
     - `aiApi.scanEnemy(ship)`: Get information (distance and angle) about the player’s ship.
     - `aiApi.getX(ship)`, `aiApi.getY(ship)`, `aiApi.getAngle(ship)`: Retrieve the ship’s current position and orientation.
     
3. **Load the AI Code:**  
   Click the **Run Code** button to load your custom AI. Errors during loading will be displayed in the output area.

## Running the Game

1. **Open the Game:**  
   Launch the `index.html` file in your web browser. The game initializes on an HTML5 canvas.

2. **Game Environment:**  
   - The canvas is set to 800x600 pixels.
   - Ships wrap around the screen edges.
   - Bullets are removed when they exit the canvas boundaries.

3. **Enjoy the Gameplay:**  
   Use the controls to maneuver your ship, engage the enemy, and modify the AI for unique challenges.

## Additional Information
- The game logic, including ship movement, bullet handling, collision checking, and AI code integration, is implemented in `game.js`.
- Players can experiment with different AI strategies by modifying how the enemy ship reacts, offering endless replayability.

Enjoy the game and have fun creating your own AI strategies!
