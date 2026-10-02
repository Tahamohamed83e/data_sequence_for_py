# Python Tuple — Cheat Sheet

## 1. Creating a Tuple

```python
numbers = (10, 20, 30, 40)
names = ("Ali", "Mona", "Omar")
```

Single-element tuple:

```python
x = (10,)
```

> The comma is required.

---

## 2. Accessing Elements

### Indexing

```python
numbers[0]
numbers[-1]
```

### Slicing

```python
numbers[1:3]
numbers[:3]
numbers[2:]
numbers[::-1]
```

---

## 3. Tuple is Immutable

You cannot modify an existing element.

```python
numbers[0] = 100
```

This causes:

```text
TypeError
```

You also cannot use:

```python
numbers.append(50)
numbers.remove(20)
numbers.sort()
```

---

## 4. Searching

### `in`

```python
20 in numbers
```

### `not in`

```python
100 not in numbers
```

### `index()`

```python
numbers.index(20)
```

### `count()`

```python
numbers.count(20)
```

---

## 5. Useful Functions

```python
len(numbers)
sum(numbers)
max(numbers)
min(numbers)
```

---

## 6. Looping

```python
for number in numbers:
    print(number)
```

With index:

```python
for i, number in enumerate(numbers):
    print(i, number)
```

---

## 7. Tuple Unpacking

```python
person = ("Taha", 20, "AI")

name, age, major = person
```

Now:

```python
name     # "Taha"
age      # 20
major    # "AI"
```

---

## 8. Converting Between List and Tuple

### Tuple → List

```python
numbers_list = list(numbers)
```

### List → Tuple

```python
numbers_tuple = tuple([1, 2, 3])
```

---

## 9. Tuple Concatenation

```python
a = (1, 2)
b = (3, 4)

result = a + b
```

Result:

```python
(1, 2, 3, 4)
```

---

## 10. Tuple Repetition

```python
numbers = (1, 2)

result = numbers * 3
```

Result:

```python
(1, 2, 1, 2, 1, 2)
```

---

## 11. When to Use a Tuple

Use a Tuple when:

* The data should not change.
* You want a fixed collection of values.
* You want to represent a fixed structure.

Example:

```python
point = (10, 20)
```

---

## 12. Most Important Methods

Tuple has only two main methods:

| Method    | Purpose           |
| --------- | ----------------- |
| `count()` | Count occurrences |
| `index()` | Find index        |

---

## Quick Mental Model

```text
TUPLE
│
├── Ordered
├── Immutable
├── Allows duplicates
├── Supports indexing
└── Supports slicing
```

### List vs Tuple

```text
List  → Mutable
Tuple → Immutable
```
