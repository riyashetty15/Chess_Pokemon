# AI-Powered Minimax Strategy for Game Optimization

### Overview
This project implements an AI-driven board game strategy using the Minimax Algorithm with Alpha-Beta Pruning. The approach is tailored to simulate the behavior of different game pieces—Pichu, Pikachu, and Raichu—inspired by chess-like movement and interaction rules. The goal is to efficiently determine optimal moves that maximize player advantage while minimizing opponent opportunities.

### Approach
The solution is based on the Minimax Algorithm combined with Alpha-Beta Pruning to optimize both game strategy and execution time. This technique ensures that:

**Best Moves:** The algorithm evaluates all possible moves up to a specified depth in the decision tree to determine the optimal move.<br>
**Pruning Unnecessary Paths:** Alpha-beta pruning eliminates irrelevant branches to the outcome, significantly reducing computational overhead.<br>
**Dynamic Depth:** The depth of exploration can be tuned to balance performance and accuracy.<br>

### Execution Details
Game Pieces:

1. Pichu: <br>
- Moves diagonally forward, similar to a chess bishop.
- Captures opponent pieces by jumping over them.
- Replaces the captured piece with an empty space (".") and moves to the next diagonal cell.

2. Pikachu:
- Moves one or two steps forward, left, or right, similar to a chess rook.
- Captures opponent pieces (Pichu or Pikachu) by jumping over them and replacing them with an empty space.

3. Raichu:
- Created when Pichu or Pikachu reaches the opposite side of the board.
- Moves in all eight directions—north, south, east, west, and diagonals.
- Captures opponent pieces in any of these directions.
  
### Key Functions:

**Pichu Function:** Checks diagonally for opponent pieces, captures them, and advances the piece.<br><br>
**Pikachu Function:** Identifies and captures opponent pieces in forward, left, or right directions.<br><br>
**Raichu Function:** Evaluates all eight possible directions and computes both moves and captures.<br><br>
Each function ensures valid moves are made while keeping track of captured pieces. <br>

### Minimax Algorithm with Alpha-Beta Pruning:

1. Starts by evaluating the current node as a maximizing or minimizing player.
2. Computes the best value for each move using the formula:
   - For maximizing nodes: best_value = max(best_value, calculated_value)
   - For minimizing nodes: best_value = min(best_value, calculated_value)

**Note: Alpha and beta values are updated to prune irrelevant paths. Incorporates "backtracking" to update the game board and simulate move outcomes.**
<br>
### Features

1. Optimized Decision Making: Minimax ensures the best possible move by considering both player and opponent strategies.
2. Adaptive Game Logic: Incorporates custom rules for movement and captures for Pichu, Pikachu, and Raichu.
3. Efficient Execution: Alpha-beta pruning significantly reduces computational complexity.
4. Dynamic Gameplay: The algorithm adapts to game states and updates moves accordingly.
   
### How It Works
**Input:** A game board with player and opponent pieces.<br>
**Processing:**
1. Evaluate possible moves using Pichu, Pikachu, and Raichu rules.
2. Use the Minimax Algorithm to explore potential outcomes.
3. Prune unnecessary branches to speed up decision-making.<br>
### Output:
- Optimal move for the player.
- Updated board state.
- Number of opponent pieces captured.
### Applications
- Board game AI.
- Optimization problems in gaming strategies.
Teaching advanced AI concepts like Minimax and Alpha-Beta Pruning.
