# Breadth First Search (BFS)

### 🔥 Difficulty: Easy
### ⏱ Time Complexity: O(V + E)
### 📦 Space Complexity: O(V)

## 📝 Problem
Explain BFS traversal of a graph.

## 💡 Approach
Use queue data structure and visit nodes level by level.

## 💻 Code

```python
from collections import deque

def bfs(graph, start):
    visited = set()
    queue = deque([start])

    while queue:
        node = queue.popleft()
        if node not in visited:
            print(node)
            visited.add(node)
            queue.extend(graph[node])
