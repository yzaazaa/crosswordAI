# Crossword AI

This project implements an AI-powered crossword puzzle solver that leverages constraint satisfaction problems (CSP) to generate valid crossword solutions efficiently.

## Features

- **Backtracking Search**: Implements backtracking to systematically explore possible solutions.
- **Constraint Propagation**: Ensures variable assignments satisfy crossword constraints (e.g., word length and overlapping characters).
- **AC3 Algorithm**: Enforces arc consistency, pruning invalid options early to optimize the solving process.
- **Customizable Puzzle**: Accepts various crossword structures and word lists as inputs.

## Files

- `crossword.py`: Contains the main logic for defining the crossword structure, constraints, and solving the puzzle.
- `generate.py`: A script to create and solve a crossword puzzle.
- `data/`: Contains crossword structures and word lists for testing.

## How It Works

1. **Define the Puzzle**: The puzzle is represented as a grid where each cell can either be a blank (to fill) or a block.
2. **Input Word List**: A list of valid words that can be used to fill the puzzle.
3. **Constraint Satisfaction**: The solver assigns words to variables (blank spaces) while satisfying the constraints:
   - Words must fit within their respective slots.
   - Overlapping cells must have matching characters.

### Example

Given the crossword structure:

```
# _ _ #
_ _ _ _
# _ _ #
```

And a word list: `["cat", "bat", "rat"]`

The solver generates a solution where the words fit into the grid, adhering to constraints.

## Setup

1. Clone the Repository:
```bash
git clone https://github.com/yzaazaa/crosswordAI
cd crosswordAI
python3 -m venv venv
source venv/bin/activate # On Windows use `venv\Scripts\activate`
```
2. Install Dependencies

```bash
pip install -r requirements.txt
```
3. Run the script:
```bash
python3 generate.py [structure.txt] [words.txt] --optional [ouptut.png] # To generate an image
```

## Key Concepts

- **Constraint Satisfaction Problem (CSP)**: The project demonstrates how AI can solve CSPs using backtracking and consistency enforcement.
- **Arc Consistency (AC3)**: This algorithm reduces the search space by ensuring binary constraints are satisfied between variables.
- **Backtracking Optimization**: By combining AC3 and backtracking, the solver achieves efficient puzzle-solving.

## Customization

- Modify the `data/structure.txt` file to create your crossword grid.
- Add your word list to `data/words.txt`.

## License

This project is part of the CS50 AI curriculum and is provided under the [CS50 License](https://cs50.harvard.edu/ai/2024/).

