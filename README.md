## Chess-AI

This project involves coding of Chess AI which can play intelligently with humans by the use of two very specific algorithm MINIMAX ALGORITHM and ALPHA BETA PRUNING.
Game can be played on the terminal with given set of rules and restrictions for the game which can be found in help section of the game.

### Breaking down the Minimax Algorithm:

The minimax algorithm is a decision-making algorithm commonly used in two-player games with perfect information, such as chess. It explores the possible outcomes of each move to find the optimal move for the current player, assuming that the opponent also plays optimally. The goal is to minimize the possible loss for the worst-case scenario.

- Initialization:
    - Move best_move; -> Creates an object of type Move named best_move to store information about the best move.
    - best_move.score = -1000000 + 2000000 * minimize; -> Initializes the initial score of the best move. The large negative value indicates an initial worst-case scenario.

- Base Case:
    - if (0 == depth) { best_move.score = score(); return best_move; } -> If the specified depth is zero, the function calculates the score of the current board position using the score() function and             returns the result. This is the base case that stops the recursion.

- Recursive Exploration:
    - The function uses a nested loop to iterate over all possible moves (from and to) for the current player.
    - A temporary ChessBoard called branch is created as a copy of the current board, and the move is made on this temporary board.
    - The minimax function is recursively called on the temporary board with reduced depth (depth - 1) and the opposite value of minimize.

- Updating Best Move:
    - The algorithm then compares the score of the current option with the score of the current best move. If the current option is better (higher score for the maximizing player or lower score for the minimizing player), the best move is updated with the information from the current option.
Final Result:

After exploring all possible moves, the function returns the information about the best move found.

This process is repeated recursively, exploring the game tree until the specified depth is reached. The algorithm assumes that both players make optimal moves at each step and aims to find the best move for the current player based on the evaluation of resulting board positions.
