# Cube Sum Finder

This Python script finds pairs of numbers whose cubes sum up to a given target number.

## Errors and Fixes
### Errors in the Original Code:
1. **Missing Colon in Function Definition:**
   - `def find_cube_pairs(target)` → `def find_cube_pairs(target):`
2. **Incorrect Exponentiation Operator (`***` instead of `**`)**
   - `max_num = round(targ *** (1/3))` → `max_num = round(target ** (1 / 3))`
3. **Incorrect Function Calls (`ranges` instead of `range`)**
   - `for a in ranges(1, max_num + 1)` → `for a in range(1, max_num + 1)`
4. **Incorrect Variable Names:**
   - `targ` → `target`
   - `sol.append((a, b));` → `solutions.append((a, b))`
   - `pair` → `pairs` in the loop
5. **Incorrect Print Statement (`printf` does not exist in Python)**
   - `printf("Valid cube pairs for 1728:")` → `print("Valid cube pairs for 1729:")`
   - `printf(f" → {a}³ + {b}³ = {a**2} + {b**2} = 1728")` → `print(f" → {a}³ + {b}³ = {a**3} + {b**3} = 1729")`
6. **Trailing Comma in Assignment**
   - `pairs = find_cube_pairs(1729),` → `pairs = find_cube_pairs(1729)`

## Fixed Code
```python
def find_cube_pairs(target):
    solutions = []
    max_num = round(target ** (1 / 3))

    for a in range(1, max_num + 1):
        for b in range(a, max_num + 1):
            if a**3 + b**3 == target:
                solutions.append((a, b))
    return solutions

pairs = find_cube_pairs(1729)
print("Valid cube pairs for 1729:")
for a, b in pairs:
    print(f" → {a}³ + {b}³ = {a**3} + {b**3} = 1729")
```

## Running the Script
Run the script in a terminal or an IDE supporting Python:
```sh
python cube_pairs.py
```
