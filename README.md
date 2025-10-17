# Indian Cities Monopoly AI Simulation

This project is a minimalist, single-file web application that simulates a basic Monopoly-like game using Indian cities as properties. The game is entirely driven by a simple AI, allowing the user to observe its progress, property acquisition, and financial management.

## How to Use

1.  **Download/Save:** Save the `index.html` content to a file named `index.html` on your computer.
2.  **Open in Browser:** Open the `index.html` file using any modern web browser (e.g., Chrome, Firefox, Edge).
3.  **Start Simulation:** Click the "Start Simulation" button to begin the AI's game.
4.  **Observe:** Watch the AI player's money, current turn, and portfolio update in real-time. The "Game Log" will record the AI's actions (dice rolls, property purchases, sales).
5.  **Adjust Speed:** Use the "Simulation Speed" slider to make the turns happen faster or slower.
6.  **Stop Simulation:** Click "Stop Simulation" to pause the game at any time. You can resume by clicking "Start Simulation" again.
7.  **Restart:** To restart the simulation from the beginning, simply refresh the browser page.

## Code Explanation

This application is built using only HTML and vanilla JavaScript, emphasizing simplicity and a single-file structure.

*   **HTML (`index.html`):** Sets up the basic page layout, including:
    *   A header for the title.
    *   A "Controls" section with buttons to start/stop the simulation and a speed slider.
    *   A "AI Player Status" section displaying the AI's current money, turn number, and position on the board.
    *   An "AI Portfolio" section listing all properties currently owned by the AI.
    *   A "Game Log" section that records all actions taken by the AI during the simulation.
    *   Inline CSS for basic styling to enhance readability and user experience.

*   **JavaScript:** Contained within a `<script>` tag in `index.html`, it manages the entire game logic:
    *   **`initialProperties`:** An array defining the Indian cities, their base prices, and rents.
    *   **`propertiesOnBoard`:** A dynamic array representing the game board, where each property can have an `owner` status.
    *   **Game State Variables:** `aiMoney`, `aiPosition`, `turnCount`, `gameLog`, `gameIntervalId`, and `simulationSpeed` track the current state of the game.
    *   **`initGame()`:** Resets all game state variables and prepares the board for a new simulation.
    *   **`addLog()` & `updateUI()`:** Functions responsible for updating the displayed information (money, portfolio, log) on the web page.
    *   **`rollDice()`:** Generates a random number (1-6) simulating a dice roll.
    *   **`aiDecideToBuy(property)`:** Implements the AI's buying logic. The AI will attempt to buy an unowned property if its current money is sufficiently high (e.g., 1.5 times the property price).
    *   **`aiDecideToSell()`:** Implements the AI's selling logic. If the AI's money drops below a certain negative threshold, it will sell its cheapest owned property for half price to try and recover financially.
    *   **`takeTurn()`:** The core game loop function. It's executed every `simulationSpeed` milliseconds. In each turn, the AI:
        1.  Rolls dice and moves its position.
        2.  Checks the property it landed on.
        3.  Decides whether to buy an unowned property.
        4.  Receives a small income for general simulation progression.
        5.  Assesses if it needs to sell properties to avoid severe debt.
        6.  Updates the UI with all changes.
    *   **`startGame()` & `stopGame()`:** Control the `setInterval` that drives the `takeTurn()` function, starting or pausing the simulation.
    *   **Event Listeners:** Attach functionality to the "Start Simulation" and "Stop Simulation" buttons, and the "Simulation Speed" slider.

The AI's decision-making is rule-based and deterministic, providing a predictable yet engaging simulation of a basic Monopoly game.

## License

This project is licensed under the MIT License.