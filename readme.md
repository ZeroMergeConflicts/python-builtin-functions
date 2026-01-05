![BANNER IMAGE](assets/images/banner.png)

## `abs(x)`

**Signature:** `abs(x)`<br>
**Returns:** absolute value of a number (int, float, complex magnitude)

**Examples**

```py
# Integers and floats
abs(-5)           # -> 5
abs(3.14)         # -> 3.14
abs(-0)           # -> 0

# Complex numbers (returns magnitude)
abs(3+4j)         # -> 5.0  (sqrt(3^2+4^2))
abs(-1j)          # -> 1.0

# Practical pattern: distance between two points
def distance(a, b):
    return abs(b - a)

distance(10, 25)  # -> 15
```

**Detailed Explanation:**
- For integers/floats: returns the non-negative numeric value.
- For complex numbers: returns the **magnitude** (always a float), computed as √(real² + imag²).
- Works with any numeric type that defines `__abs__()`.
- The result has the same type as input (except complex → float).

**Use-cases:**
- Distance/error calculations in algorithms
- Normalizing values (e.g., confidence scores)
- Computing magnitude of force/velocity vectors
- Handling signed differences

**Tips & Pitfalls:**
- `abs()` on complex returns float, not complex.
- For arrays/NumPy: use `numpy.abs()` for vectorized efficiency.
- Cannot use on incompatible types (e.g., strings); raises `TypeError`.
- `abs(None)` raises `TypeError`; check types first in dynamic code.
