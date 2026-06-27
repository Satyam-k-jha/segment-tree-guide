# Segment Tree

A **Segment Tree** is an advanced data structure used for efficiently answering range queries and performing updates on an array. It supports operations like range sum, minimum, maximum, GCD, XOR, etc., in logarithmic time.

## Features

- Fast range queries
- Point updates
- Supports multiple operations:
  - Sum
  - Minimum
  - Maximum
  - GCD
  - XOR (can be customized)
- Time-efficient for competitive programming and large datasets

---

## Time Complexity

| Operation | Complexity |
|-----------|------------|
| Build | O(n) |
| Range Query | O(log n) |
| Point Update | O(log n) |
| Space | O(4n) |

---

## How It Works

A Segment Tree is a binary tree where:

- Each leaf node represents one element of the array.
- Each internal node stores information (sum/min/max/etc.) about a range of elements.
- Queries and updates only visit relevant nodes, making operations efficient.

Example:

Array:

```
[1, 3, 5, 7, 9, 11]
```

Segment Tree (Sum):

```
                36
             /      \
           9          27
         /   \      /    \
        4     5    16     11
       / \         / \
      1   3       7   9
```

---

## Supported Operations

### Build Tree

Constructs the Segment Tree from the input array.

```cpp
build(1, 0, n - 1);
```

### Range Query

Returns the result over a given range.

```cpp
query(1, 0, n - 1, l, r);
```

### Point Update

Updates a single index.

```cpp
update(1, 0, n - 1, index, value);
```

---

## Example

Input Array

```text
1 3 5 7 9 11
```

Query

```text
Sum from index 1 to 3
```

Output

```text
15
```

Update

```text
Update index 2 to 10
```

Updated Array

```text
1 3 10 7 9 11
```

Query Again

```text
Sum from index 1 to 3
```

Output

```text
20
```

---

## Applications

- Range Sum Query
- Range Minimum Query (RMQ)
- Range Maximum Query
- Frequency Counting
- Dynamic Programming Optimizations
- Competitive Programming
- Database Range Operations

---

## Advantages

- Efficient range queries
- Fast updates
- Flexible for different associative operations
- Much faster than brute force for repeated queries

---

## Limitations

- Uses extra memory (`O(4n)`)
- More complex than Prefix Sum or Fenwick Tree
- Slightly larger constant factor

---

## Folder Structure

```
Segment-Tree/
│
├── segment_tree.cpp
├── README.md
└── sample_input.txt
```

---

## References

- CP Algorithms
- GeeksforGeeks
- Competitive Programming Handbook

---

## License

This project is licensed under the MIT License.

---

⭐ If you found this repository helpful, consider giving it a star!
