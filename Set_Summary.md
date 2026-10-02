# Python Set — Cheat Sheet

## 1. Creating a Set

```python
numbers = {1, 2, 3, 4}
```

Duplicates are automatically removed:

```python
numbers = {1, 2, 2, 3, 3, 4}
```

Result:

```python
{1, 2, 3, 4}
```

---

## 2. Important: Empty Set

This:

```python
x = {}
```

creates an empty **dictionary**, not a set.

For an empty set:

```python
x = set()
```

---

## 3. Adding Elements

### `add()`

Adds one element.

```python
numbers.add(5)
```

### `update()`

Adds multiple elements.

```python
numbers.update([6, 7, 8])
```

---

## 4. Removing Elements

### `remove()`

```python
numbers.remove(3)
```

If the element does not exist, it raises an error.

### `discard()`

```python
numbers.discard(3)
```

If the element does not exist, nothing happens.

### `pop()`

```python
numbers.pop()
```

Removes an arbitrary element.

### `clear()`

```python
numbers.clear()
```

Removes everything.

---

## 5. Membership Testing

One of the most important uses of a Set:

```python
3 in numbers
```

```python
10 not in numbers
```

Sets are especially useful when you repeatedly need to ask:

```text
"Does this element exist?"
```

---

# Set Operations

Suppose:

```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}
```

---

## 6. Union

All elements from both sets.

```python
A | B
```

Or:

```python
A.union(B)
```

Result:

```python
{1, 2, 3, 4, 5, 6}
```

---

## 7. Intersection

Elements that exist in both sets.

```python
A & B
```

Or:

```python
A.intersection(B)
```

Result:

```python
{3, 4}
```

---

## 8. Difference

Elements in `A` but not in `B`.

```python
A - B
```

Result:

```python
{1, 2}
```

The reverse:

```python
B - A
```

Result:

```python
{5, 6}
```

---

## 9. Symmetric Difference

Elements that exist in either set, but not in both.

```python
A ^ B
```

Or:

```python
A.symmetric_difference(B)
```

Result:

```python
{1, 2, 5, 6}
```

---

# Set Relationships

## 10. `issubset()`

Checks whether all elements of one set exist in another.

```python
A.issubset(B)
```

---

## 11. `issuperset()`

Checks whether a set contains all elements of another set.

```python
A.issuperset(B)
```

---

## 12. `isdisjoint()`

Checks whether two sets have no common elements.

```python
A.isdisjoint(B)
```

---

## 13. Looping

```python
for number in numbers:
    print(number)
```

> Sets are unordered collections, so do not rely on their iteration order.

---

## 14. Set Length

```python
len(numbers)
```

---

## 15. Converting List → Set

Very useful for removing duplicates:

```python
numbers = [1, 2, 2, 3, 3]

unique_numbers = set(numbers)
```

Result:

```python
{1, 2, 3}
```

---

## 16. Set → List

```python
numbers = list(unique_numbers)
```

---

## 17. Set Comprehension

```python
squares = {x ** 2 for x in range(1, 6)}
```

Result:

```python
{1, 4, 9, 16, 25}
```

---

## 18. Common Set Patterns

### Remove Duplicates

```python
unique = set(items)
```

### Fast Membership Checking

```python
items_set = set(items)

if target in items_set:
    print("Found")
```

### Find Common Elements

```python
common = set_a & set_b
```

### Find Unique Elements

```python
unique_to_a = set_a - set_b
```

---

## 19. Most Important Methods

| Method                   | Purpose                  |
| ------------------------ | ------------------------ |
| `add()`                  | Add one element          |
| `update()`               | Add multiple elements    |
| `remove()`               | Remove an element        |
| `discard()`              | Remove safely            |
| `pop()`                  | Remove arbitrary element |
| `clear()`                | Remove everything        |
| `union()`                | Combine sets             |
| `intersection()`         | Find common elements     |
| `difference()`           | Find differences         |
| `symmetric_difference()` | Find non-common elements |
| `issubset()`             | Check subset             |
| `issuperset()`           | Check superset           |
| `isdisjoint()`           | Check no intersection    |

---

## Quick Mental Model

```text
SET
│
├── Unique elements
├── No duplicates
├── Mutable
├── No indexing
└── Excellent for membership & set operations
```

### Common Problem Patterns

```text
Remove duplicates       → Set
Fast membership check   → Set
Find common elements    → Intersection
Find differences        → Difference
Combine unique items    → Union
```
