# Python List — Cheat Sheet

## 1. Creating a List

```python
numbers = [10, 20, 30, 40]
names = ["Ali", "Mona", "Omar"]
mixed = [10, "Python", True, 3.5]
```

---

## 2. Accessing Elements

### Indexing

```python
numbers[0]      # 10
numbers[2]      # 30
numbers[-1]     # 40
```

### Slicing

```python
numbers[1:3]    # [20, 30]
numbers[:3]     # [10, 20, 30]
numbers[2:]     # [30, 40]
numbers[:]      # Copy of the list
numbers[::-1]   # Reverse
```

---

## 3. Adding Elements

### `append()`

Adds one element to the end.

```python
numbers.append(50)
```

```text
[10, 20, 30, 40, 50]
```

### `insert()`

Adds an element at a specific index.

```python
numbers.insert(1, 15)
```

```text
[10, 15, 20, 30, 40]
```

### `extend()`

Adds multiple elements.

```python
numbers.extend([50, 60])
```

```text
[10, 20, 30, 40, 50, 60]
```

### `append()` vs `extend()`

```python
numbers.append([50, 60])
```

Result:

```python
[10, 20, 30, 40, [50, 60]]
```

While:

```python
numbers.extend([50, 60])
```

Result:

```python
[10, 20, 30, 40, 50, 60]
```

---

## 4. Removing Elements

### `remove()`

Removes the first occurrence of a value.

```python
numbers.remove(20)
```

### `pop()`

Removes and returns an element.

```python
numbers.pop()
```

Removes the last element.

```python
numbers.pop(1)
```

Removes the element at index `1`.

### `del`

Deletes an element or a range.

```python
del numbers[1]
```

```python
del numbers[1:3]
```

### `clear()`

Removes everything.

```python
numbers.clear()
```

---

## 5. Searching

### `in`

```python
20 in numbers
```

### `not in`

```python
100 not in numbers
```

### `index()`

Returns the index of the first occurrence.

```python
numbers.index(30)
```

### `count()`

Counts how many times a value appears.

```python
numbers.count(20)
```

---

## 6. Sorting

### `sort()`

Sorts the original list.

```python
numbers.sort()
```

Descending:

```python
numbers.sort(reverse=True)
```

### `sorted()`

Returns a new sorted list.

```python
new_numbers = sorted(numbers)
```

> **Important:**
> `sort()` modifies the original list.
> `sorted()` returns a new list.

---

## 7. Reversing

### `reverse()`

Reverses the original list.

```python
numbers.reverse()
```

### Slicing

Creates a reversed copy.

```python
reversed_numbers = numbers[::-1]
```

---

## 8. Useful Built-in Functions

```python
len(numbers)
sum(numbers)
max(numbers)
min(numbers)
```

Example:

```python
numbers = [10, 20, 30]

len(numbers)     # 3
sum(numbers)     # 60
max(numbers)     # 30
min(numbers)     # 10
```

---

## 9. Looping

### Basic Loop

```python
for number in numbers:
    print(number)
```

### Loop with Index

```python
for i in range(len(numbers)):
    print(i, numbers[i])
```

### `enumerate()`

```python
for i, number in enumerate(numbers):
    print(i, number)
```

---

## 10. List Concatenation

```python
a = [1, 2, 3]
b = [4, 5, 6]

result = a + b
```

Result:

```python
[1, 2, 3, 4, 5, 6]
```

---

## 11. Repetition

```python
numbers = [1, 2]

result = numbers * 3
```

Result:

```python
[1, 2, 1, 2, 1, 2]
```

---

## 12. Copying

### Shallow Copy

```python
new_list = numbers.copy()
```

Or:

```python
new_list = numbers[:]
```

---

## 13. List Comprehension

Create a new list from another iterable.

```python
squares = [x ** 2 for x in numbers]
```

With a condition:

```python
even_numbers = [x for x in numbers if x % 2 == 0]
```

---

## 14. Common List Patterns

### Filtering

```python
result = []

for item in items:
    if condition:
        result.append(item)
```

### Finding Maximum

```python
maximum = max(numbers)
```

### Removing Duplicates

```python
unique = list(set(numbers))
```

> Note: Converting to a set does not preserve the original order in a general sense.

---

## 15. Most Important Methods

| Operation          | Method      |
| ------------------ | ----------- |
| Add one item       | `append()`  |
| Add multiple items | `extend()`  |
| Insert at index    | `insert()`  |
| Remove by value    | `remove()`  |
| Remove by index    | `pop()`     |
| Delete             | `del`       |
| Remove everything  | `clear()`   |
| Find index         | `index()`   |
| Count occurrences  | `count()`   |
| Sort               | `sort()`    |
| Reverse            | `reverse()` |
| Copy               | `copy()`    |

---

## Quick Mental Model

```text
LIST
│
├── Ordered
├── Mutable
├── Allows duplicates
├── Supports indexing
└── Supports slicing
```
