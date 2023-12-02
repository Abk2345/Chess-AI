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

Interview Prep:
AI-based Chess Player [Apr '21]

- Developed an AI-based chess player in **C++**, an interactive game which can be played against the application through the terminal
- Implemented **minimax algorithm** to decide moves against the player. and **alpha-beta pruning** to optimize the runtime of the game
- In each state, the points gained after performing any of the stored possible legal moves for the pieces is compared to select **optimal** move

Questions:

What is minimax algorithm?

Minimax is a kind of **[backtracking](https://www.geeksforgeeks.org/tag/backtracking/)** algorithm that is used in decision making and game theory to find the optimal move for a player, assuming that your opponent also plays optimally. It is widely used in two player turn-based games such as Tic-Tac-Toe, Backgammon, Mancala, Chess, etc.In Minimax the two players are called maximizer and minimizer. The **maximizer** tries to get the highest score possible while the **minimizer** tries to do the opposite and get the lowest score possible.Every board state has a value associated with it. In a given state if the maximizer has upper hand then, the score of the board will tend to be some positive value. If the minimizer has the upper hand in that board state then it will tend to be some negative value. The values of the board are calculated by some heuristics which are unique for every type of game.

minimax is a kind of backracking algorithm used in game theory. it is usually used to select the best move from given options of moves, and it is used commonly for two player game. How it works is it gives a tag of maximising player and minimising player to both of it’s players, while recuring, one try to maximise while other tries to minimise the score optimally to reach the optimal solution

What is alpha beta pruning?

it is a technique which is used to prune out un-advantageous states which does not needs to be computed for a particular state to select it’s best move

Which concept of coding did u use, elaborate?

it is coded in c++ using object oriented programming, 

what did u consider as parameters?

depth of exploration for the search algorithm for optimisation, and the input given by user, with a fiixed priority value for every of chess pieces

what is the depth consideration?

depth is considered as 2

what will happen if u increase the depth?

time complexity will increase by factor of 2, and the algorithm will become more accurate, since the time cost tradeoff is not profitable, we choose depth=2

can you explain the code?

yes sure, open the code and explain briefly
