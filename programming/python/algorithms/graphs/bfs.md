---
description: Przeszukiwanie grafu wszerz
---

# BFS

## Problem description

{% content-ref url="../../../../algorithms/graphs/bfs.md" %}
[bfs.md](../../../../algorithms/graphs/bfs.md)
{% endcontent-ref %}

## Implementation

{% code overflow="wrap" lineNumbers="true" %}
```python
from typing import List


def bfs(graph: List[List[int]], visited: List[bool], node: int):
    queue = [node]

    while len(queue) > 0:
        node = queue[0]
        queue.pop(0)
        
        if visited[node]:
            continue

        visited[node] = True
        print(f'Odwiedzony wierzchołek: {node}')

        for new_node in graph[node]:
            if not visited[new_node]:
                queue.append(new_node)


graph = [
	[1, 6],
	[0, 6, 3, 2],
	[1, 3],
	[2, 1, 6, 4, 5],
	[3, 5],
	[4, 3, 6],
	[0, 1, 3, 5],
]

visited = [False for _ in range(len(graph))]

bfs(graph, visited, 0)
```
{% endcode %}

### Link do implementacji

{% embed url="https://ideone.com/X87JSj" %}
BFS
{% endembed %}
