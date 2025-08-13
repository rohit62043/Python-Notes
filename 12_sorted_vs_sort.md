# Difference Between `sorted()` and `.sort()` in Python

## 1. `sorted()`

- **Type**: Built-in function (works on any iterable — list, tuple, string, dict, set, etc.)
- **Returns**: A **new sorted list** (does not modify the original object)
- **Usage**:

```python
numbers = [4, 2, 9, 1]
new_list = sorted(numbers)
print(new_list)   # [1, 2, 4, 9]
print(numbers)    # [4, 2, 9, 1]  (unchanged)
```

- Can be used on immutable objects (like tuples or strings).

---

## 2. `.sort()`

- **Type**: List method (works only on lists)
- **Returns**: `None` (sorts in place — modifies the list itself)
- **Usage**:

```python
numbers = [4, 2, 9, 1]
numbers.sort()
print(numbers)    # [1, 2, 4, 9]
```

- **Faster** than `sorted()` when sorting a list because it avoids creating a new list.

---

## Common Parameters (Both Support These)

- `` → Sort in descending order
- `` → Sort by custom logic

```python
words = ["banana", "apple", "cherry"]

# Using sorted
sorted_words = sorted(words, key=len)      # ['apple', 'banana', 'cherry']

# Using sort
words.sort(key=len, reverse=True)          # ['banana', 'cherry', 'apple']
```

---

## Summary Table

| Feature                           | `sorted()`                         | `.sort()`                  |
| --------------------------------- | ---------------------------------- | -------------------------- |
| Works on                          | Any iterable                       | Only lists                 |
| Returns                           | New sorted list                    | None (modifies original)   |
| Modifies original                 | ❌ No                               | ✅ Yes                      |
| Usable with tuple/string/dict/set | ✅ Yes                              | ❌ No                       |
| Performance                       | Slightly slower (creates new list) | Slightly faster (in-place) |

