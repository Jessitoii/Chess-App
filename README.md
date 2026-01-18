♟️ **Python Chess App (PyQt5 Implementation)**
----------------------------------------------

A fully functional, graphical Chess Application built from scratch using **Python** and **PyQt5**.

Unlike standard chess apps that rely on libraries like python-chess for game logic, this project features a **custom-built chess engine**, demonstrating advanced Object-Oriented Programming (OOP) principles and algorithm design to handle move validation, board state management, and complex rules like Castling.

🚀 Features
-----------

*   **Custom Game Engine:** All mechanics (move generation, legality checks, board representation) are implemented manually without external logic libraries.
    
*   **Modern GUI:** A responsive and interactive interface built with **PyQt5**.
    
*   **OOP Architecture:** Robust class hierarchy where every piece (Pawn, Rook, Knight...) inherits from a base Piece class with unique movement behaviors.
    
*   **Rule Implementation:**
    
    *   ✅ Legal Move Validation
        
    *   ✅ Check & Checkmate Detection
        
    *   ✅ Castling (King-side & Queen-side)
        
    *   ✅ Turn-based State Management
        
*   **Asset Integration:** Custom graphical assets for board and pieces.
    

🛠️ Technology Stack
--------------------

*   **Language:** Python 3.x
    
*   **GUI Framework:** PyQt5
    
*   **Logic:** Pure Python (Custom Algorithms)
    

📂 Project Structure
--------------------

The project is structured to separate User Interface (UI) from Game Logic (Mechanics).

```text   src/chess/  ├── main_window.py            # Application Entry Point  ├── ui_components/  │   ├── board.py              # Custom UI Widget for rendering the board  │   └── round_widget.py       # Turn indicator widget  └── mechanics/      ├── game.py               # Core Game Loop & Board State Manager      ├── piece.py              # Base Class for all pieces      └── pieces/               # Polymorphic Piece Implementations          ├── king.py          ├── queen.py          ├── rook.py          ├── bishop.py          ├── knight.py          └── pawn.py
```

⚙️ How It Works (Under the Hood)
--------------------------------

### 1\. Board Representation

The board is managed as a dictionary-based coordinate system (e.g., "e4": {piece\_object}") within the Game class. This allows for O(1) lookups and flexible state management.

### 2\. Move Validation

Instead of using a pre-built move generator, each piece class (src/chess/mechanics/pieces/) calculates its own pseudo-legal moves based on its geometry. The Game class then filters these moves by simulating them to ensure the King is not left in check.

### 3\. The "Mirror" Logic

The application distinguishes between the **Visual Board** (UI) and the **Logical Board** (Backend). User interactions on the UI trigger events in the Game class, which validates the move before updating the UI state.

📥 Installation & Usage
-----------------------

1.  ```bash
    git clone https://github.com/yourusername/python-chess-app.gitcd python-chess-app
    ```
2. ```bash
   Bashpip install PyQt5
   ```
    
3.  ```bash
    python src/chess/main\_window.py
    ```
    

📸 Screenshots
--------------

_(You can add screenshots of your application here)_

🤝 Contribution
---------------

This project is open for educational purposes. Feel free to fork and improve the engine efficiency or add features like _En Passant_ or _Pawn Promotion_ UI dialogs.

📝 License
----------

This project is licensed under the MIT License.
