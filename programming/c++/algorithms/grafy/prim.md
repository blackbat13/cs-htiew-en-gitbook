# Prim

## Problem description

{% content-ref url="../../../../algorithms/grafowe/prim.md" %}
[prim.md](../../../../algorithms/grafowe/prim.md)
{% endcontent-ref %}

## Implementation

```cpp
#include <iostream>
#include <vector>
#include <queue>
#include <climits>

using namespace std;

/// Structure for representing an edge in a weighted graph
struct edge {
    int from;
    int to;
    int distance;

    edge(int from, int to, int distance) {
        this->from = from;
        this->to = to;
        this->distance = distance;
    }

    bool operator<(const edge &rhs) const {
        return distance > rhs.distance;
    }
};

/// Incidence list of the weighted graph
vector<vector<edge> > graph;

vector<edge> min_spanning_tree;

vector<bool> visited;

/// Prepares example graph adding vertices to incidence list
void prepareExampleGraph() {
    graph = vector<vector<edge> >(7);
    graph[0].push_back(edge(0, 1, 5));
    graph[0].push_back(edge(0, 6, 5));

    graph[1].push_back(edge(1, 0, 5));
    graph[1].push_back(edge(1, 6, 5));
    graph[1].push_back(edge(1, 3, 3));
    graph[1].push_back(edge(1, 2, 3));

    graph[2].push_back(edge(2, 1, 3));
    graph[2].push_back(edge(2, 3, 1));

    graph[3].push_back(edge(3, 2, 1));
    graph[3].push_back(edge(3, 1, 3));
    graph[3].push_back(edge(3, 6, 3));
    graph[3].push_back(edge(3, 4, 5));
    graph[3].push_back(edge(3, 5, 4));

    graph[4].push_back(edge(4, 3, 5));
    graph[4].push_back(edge(4, 5, 2));

    graph[5].push_back(edge(5, 4, 2));
    graph[5].push_back(edge(5, 3, 4));
    graph[5].push_back(edge(5, 6, 5));

    graph[6].push_back(edge(6, 0, 5));
    graph[6].push_back(edge(6, 1, 5));
    graph[6].push_back(edge(6, 3, 3));
    graph[6].push_back(edge(6, 5, 5));
}

void prim(int node) {
    priority_queue<edge> edges;

    min_spanning_tree = vector<edge>();
    visited = vector<bool>(graph.size());
    visited[node] = true;

    for (int i = 0; i < graph[node].size(); i++) {
        edges.push(graph[node][i]);
    }

    while (!edges.empty()) {
        edge current = edges.top();
        edges.pop();

        if (visited[current.to]) {
            continue;
        }

        visited[current.to] = true;
        min_spanning_tree.push_back(current);

        for (int i = 0; i < graph[current.to].size(); i++) {
            edge next = graph[current.to][i];
            if (!visited[next.to]) {
                edges.push(next);
            }
        }
    }
}

int main() {
    prepareExampleGraph();

    prim(0);

    for (int i = 0; i < min_spanning_tree.size(); i++) {
        edge current = min_spanning_tree[i];
        cout << current.from << " <-(" << current.distance << ")-> " << current.to << endl;
    }

    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/PR4Noz" %}
Algorytm Prima
{% endembed %}

### Implementation descriptioni

Na pocz??tku definiujemy struktur?? `edge` do reprezentacji kraw??dzi grafu (**linia 9**). Poniewa?? mamy do czynienia z grafem wa??onym, w strukturze przechowujemy trzy warto??ci: 

* wierzcho??ek pocz??tkowy kraw??dzi - zmienna `from` (**linia 10**),
* wierzcho??ek docelowy kraw??dzi - zmienna `to` (**linia 11**),
* waga/d??ugo???? kraw??dzi - zmienna `distance` (**linia 12**)

Dla u??atwienia definiujemy tak??e konstruktor dla naszej struktury (**linia 14**). Poniewa?? kraw??dzie chcemy przechowywa?? w kolejce priorytetowej, musimy tak??e zdefiniowa?? `operator<` do por??wnywania kraw??dzi (**linia 20**). Warto tutaj zwr??ci?? uwag?? na to, ??e kolejka priorytetowa z stl jest typu max, co oznacza, ??e domy??lnie zwraca??aby nam kraw??d?? o najwi??kszej wadze. Poniewa?? do algorytmu Prima potrzebujemy pobiera?? kraw??dzie o najmniejszej wadze najpierw, odwracamy porz??dek kraw??dzi podczas por??wnywania ich wagi (**linia 21**).

![Przyk??adowy graf wykorzystany w implementacji](../../../../.gitbook/assets/example_graph_weighted.png)

{% embed url="http://graphonline.ru/en/?graph=DZlFqSBPNgdHwNXK" %}
