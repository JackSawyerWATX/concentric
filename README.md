# Concentric

A simple Python script that generates a concentric square pattern using ASCII numbers.

## What It Is

`concentric.py` is a compact program that creates a 2D grid of numbers arranged in concentric squares. Each layer represents a distance from the center, with the innermost square showing `1`, the next layer showing `2`, and so on.

## How It Works

The script uses a mathematical approach to generate the pattern:

1. **Grid Size**: Set by the variable `n`, the total grid is `(2*n - 1) × (2*n - 1)` in size
   - For `n=4`, this creates a 7×7 grid

2. **Distance Calculation**: For each position `(i, j)` in the grid, it calculates the maximum of:
   - Distance from top/bottom edges: `abs(i - n + 1)`
   - Distance from left/right edges: `abs(j - n + 1)`
   - This value + 1 determines the concentric layer number

3. **Output**: Numbers are printed with spaces between them and a newline after each row

### Example Output (n=4)
```
4 4 4 4 4 4 4 
4 3 3 3 3 3 4 
4 3 2 2 2 3 4 
4 3 2 1 2 3 4 
4 3 2 2 2 3 4 
4 3 3 3 3 3 4 
4 4 4 4 4 4 4 
```

## How to Run

### Basic Usage
```bash
python concentric.py
```

This will display the concentric square pattern with the default size (n=4).

### Modifying the Size
Edit the first line of the script to change the grid size:
```python
n=8  # Creates a 15×15 grid instead
```

Then run:
```bash
python concentric.py
```

### Requirements
- Python 3.x (no external dependencies required)

## Customization

To experiment with different sizes, you can modify the `n` variable:
- `n=2` → 3×3 grid
- `n=3` → 5×5 grid
- `n=4` → 7×7 grid (default)
- `n=10` → 19×19 grid
