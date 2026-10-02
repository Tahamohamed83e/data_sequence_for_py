# Python Dictionary — Cheat Sheet

## 1. Creating a Dictionary

```python
student = {
    "name": "Taha",
    "age": 20,
    "major": "AI"
}
```

The structure is:

```text
Key → Value
```

Example:

```text
"name" → "Taha"
"age"  → 20
"major" → "AI"
```

---

## 2. Accessing Values

### Using `[]`

```python
student["name"]
```

Result:

```text
"Taha"
```

### Using `get()`

```python
student.get("name")
```

If the key does not exist:

```python
student.get("phone")
```

Result:

```text
None
```

You can provide a default:

```python
student.get("phone", "Not Found")
```

---

## 3. Adding a Key

```python
student["city"] = "Beni Suef"
```

---

## 4. Updating a Value

```python
student["age"] = 21
```

The same syntax is used for adding and updating:

```python
dictionary[key] = value
```

---

## 5. `update()`

Update multiple values:

```python
student.update({
    "age": 21,
    "city": "Beni Suef"
})
```

---

## 6. Removing Items

### `pop()`

Removes a key and returns its value.

```python
student.pop("age")
```

### `popitem()`

Removes and returns the last key-value pair.

```python
student.popitem()
```

### `del`

```python
del student["age"]
```

### `clear()`

Removes everything.

```python
student.clear()
```

---

## 7. Dictionary Views

### `keys()`

Returns the keys.

```python
student.keys()
```

### `values()`

Returns the values.

```python
student.values()
```

### `items()`

Returns key-value pairs.

```python
student.items()
```

---

## 8. Looping

### Keys

```python
for key in student:
    print(key)
```

### Values

```python
for value in student.values():
    print(value)
```

### Keys + Values

```python
for key, value in student.items():
    print(key, value)
```

---

## 9. Checking if a Key Exists

```python
"name" in student
```

```python
"phone" not in student
```

> `in` checks the **keys** of a dictionary.

---

## 10. Dictionary Length

```python
len(student)
```

Returns the number of key-value pairs.

---

## 11. Dynamic Key Access

This is extremely important:

```python
char = "a"

count = {
    "a": 2,
    "b": 5
}

count[char]
```

This is equivalent to:

```python
count["a"]
```

Because:

```python
char = "a"
```

General pattern:

```python
dictionary[key]
```

---

## 12. Counting Pattern

```python
count = {}

for char in text:
    if char not in count:
        count[char] = 1
    else:
        count[char] += 1
```

Example:

```python
text = "taha"
```

Result:

```python
{
    "t": 1,
    "a": 2,
    "h": 1
}
```

---

## 13. Grouping Pattern

```python
groups = {}

for item in items:
    key = some_transformation(item)

    if key not in groups:
        groups[key] = [item]
    else:
        groups[key].append(item)
```

Example:

```python
students = {
    "Ali": "A",
    "Mona": "B",
    "Omar": "A"
}
```

Grouping by grade:

```python
groups = {}

for name, grade in students.items():
    if grade not in groups:
        groups[grade] = [name]
    else:
        groups[grade].append(name)
```

---

## 14. Dictionary Comprehension

```python
squares = {
    x: x ** 2
    for x in range(1, 6)
}
```

Result:

```python
{
    1: 1,
    2: 4,
    3: 9,
    4: 16,
    5: 25
}
```

---

## 15. Converting Dictionary Data

### Keys → List

```python
list(student.keys())
```

### Values → List

```python
list(student.values())
```

### Items → List

```python
list(student.items())
```

---

## 16. Most Important Methods

| Method      | Purpose                   |
| ----------- | ------------------------- |
| `get()`     | Access value safely       |
| `keys()`    | Get keys                  |
| `values()`  | Get values                |
| `items()`   | Get key-value pairs       |
| `update()`  | Add/update multiple items |
| `pop()`     | Remove a key              |
| `popitem()` | Remove last pair          |
| `clear()`   | Remove everything         |

---

## Quick Mental Model

```text
DICTIONARY
│
├── Key → Value
├── Keys are unique
├── Mutable
├── Access using keys
└── Excellent for lookup/counting/grouping
```

### Common Problem Patterns

```text
Counting      → Dictionary
Grouping      → Dictionary
Lookup        → Dictionary
Mapping       → Dictionary
Frequency     → Dictionary
```
