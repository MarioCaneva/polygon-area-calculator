# Polygon Area Calculator

This Python application uses object-oriented programming (OOP) principles to calculate areas, perimeters, and diagonals of polygons, particularly rectangles and squares. It supports shape visualization, dimensions adjustment, and checking how many smaller shapes fit inside larger ones.

---

## 📦 Features

- Calculate area, perimeter, and diagonal of rectangles and squares
- Visualize shapes with text-based output
- Handle square-specific logic via inheritance
- Calculate how many smaller shapes fit within larger shapes
- Output of shape descriptions

---

## 🔧 How It Works

### ✅ Rectangle Class

The `Rectangle` class contains:
- `set_width()` and `set_height()` to modify dimensions
- `get_area()`, `get_perimeter()`, `get_diagonal()` to retrieve shape properties
- `get_picture()` for visual representation (limits on dimensions for large shapes)
- `get_amount_inside()` to calculate how many smaller shapes fit within the rectangle

### ✅ Square Class

The `Square` class:
- Inherits from `Rectangle`
- Shares the same methods, but restricts dimensions to be equal
- Can adjust the side length using `set_side()`

### Example Usage

```python
rect = Rectangle(10, 5)
print(rect.get_area())         # 50
rect.set_height(3)
print(rect.get_perimeter())    # 26
print(rect)                    # Rectangle(width=10, height=3)
print(rect.get_picture())      # Visual representation

sq = Square(9)
print(sq.get_area())           # 81
sq.set_side(4)
print(sq.get_diagonal())       # 5.656854249492381
print(sq)                      # Square(side=4)
print(sq.get_picture())        # Visual representation

rect.set_height(8)
rect.set_width(16)
print(rect.get_amount_inside(sq))  # Number of squares that fit inside the rectangle
🧠 Concepts Practiced
Python classes and inheritance

Shape area and perimeter calculations

String-based visualization for shapes

Mathematical calculations using basic arithmetic operations
