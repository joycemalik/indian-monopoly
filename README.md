# Indian Cities Monopoly AI Simulation

This project simulates a simplified version of Monopoly for Indian cities, featuring an AI player. The simulation is now enhanced with a visual game board, an animated player piece, and a dice roller.

## Features

*   **AI Player Simulation:** An AI player attempts to buy properties and manage its finances.
*   **Dynamic Game Log:** Real-time updates on AI actions, property transactions, and game events.
*   **AI Portfolio:** Tracks properties currently owned by the AI.
*   **Adjustable Simulation Speed:** Control how fast the AI takes turns.
*   **Visual Game Board:** A grid-based representation of the Monopoly board with 10 Indian cities and a "START" square.
*   **Animated Player Piece:** The AI's piece moves smoothly across the board after each dice roll.
*   **Dice Roller:** A visual dice element that animates a roll and displays the result for each turn.
*   **Property Ownership Display:** Properties on the board visually indicate when they are owned by the AI.

## How to Play

1.  Open `index.html` in your web browser.
2.  Click the "Start Simulation" button to begin the AI's turns.
3.  Observe the AI's progress on the board, log, and portfolio sections.
4.  Adjust the "Simulation Speed" slider to make the AI's turns faster or slower.
5.  Click "Stop Simulation" at any time to pause the game.
6.  If the AI goes bankrupt (runs out of money and properties to sell), the simulation will stop automatically.

## AI Logic

The AI player follows a simple strategy:
*   **Buying:** Attempts to buy unowned properties if its current money is 1.5 times the property's price or more.
*   **Selling:** If the AI's money drops significantly into negative (debt), it sells its cheapest owned property for half its original price to reduce debt.
*   **Income:** Gains a fixed amount of income for each turn, with a larger bonus for passing or landing on the "START" square.

## Technical Details

*   **HTML5:** Structure of the web page.
*   **CSS3:** Styling for layout, board, player piece, dice, and animations.
    *   Uses CSS Grid for the board layout.
    *   CSS `transform` and `transition` properties are used for smooth player piece movement and dice rolling animations.
*   **JavaScript (ES6+):** Core game logic, UI updates, and animation orchestration.
    *   Uses `setInterval` to manage game turns.
    *   Leverages `async/await` with `setTimeout` to sequence dice rolling and piece movement animations, ensuring a coherent turn flow.
    *   Dynamically generates board elements and updates their states based on game events.

## Setup

No special setup is required. Simply download the `index.html` file and open it in any modern web browser.

## Future Enhancements

*   Multiple AI players.
*   More sophisticated AI decision-making (e.g., property sets, trading).
*   Visual upgrades for property upgrades (houses/hotels).
*   Sound effects for dice rolls and property transactions.
*   Detailed tooltips for board properties.
*   User interaction (e.g., letting a human player play against the AI).
*   Handling of "Chance" or "Community Chest" equivalent squares.
*   Bankrupt/game-over conditions and restart options.