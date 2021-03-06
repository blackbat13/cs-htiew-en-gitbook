---
description: Przeszukiwanie grafu wszerz
---

# BFS

## Problem description

{% content-ref url="../../../../algorithms/grafowe/bfs.md" %}
[bfs.md](../../../../algorithms/grafowe/bfs.md)
{% endcontent-ref %}

## Implementation

```cpp
#include <iostream>
#include <vector>
#include <queue>
using namespace std;

/// Incidence list of the graph
vector<vector<int> > graph;

/// True if node was visited, false otherwise
vector<bool> visited;

/// Prepares example graph adding vertices to incidence list
void prepareExampleGraph() {
    graph = vector<vector<int> >(7);
    graph[0].push_back(1);
    graph[0].push_back(6);

    graph[1].push_back(0);
    graph[1].push_back(6);
    graph[1].push_back(3);
    graph[1].push_back(2);

    graph[2].push_back(1);
    graph[2].push_back(3);

    graph[3].push_back(2);
    graph[3].push_back(1);
    graph[3].push_back(6);
    graph[3].push_back(4);
    graph[3].push_back(5);

    graph[4].push_back(3);
    graph[4].push_back(5);

    graph[5].push_back(4);
    graph[5].push_back(3);
    graph[5].push_back(6);

    graph[6].push_back(0);
    graph[6].push_back(1);
    graph[6].push_back(3);
    graph[6].push_back(5);
}

/// Iterative bfs algorithm
/// \param node - starting node to visit
void bfs(int node) {
    queue<int> nodes;

    nodes.push(node);

    while (!nodes.empty()) {
        node = nodes.front();
        nodes.pop();
        if (visited[node]) {
            continue;
        }

        visited[node] = true;
        cout << "Visited node: " << node << endl;

        for (int i = 0; i < graph[node].size(); i++) {
            int next_node = graph[node][i];
            if (!visited[next_node]) {
                nodes.push(next_node);
            }
        }
    }
}

int main() {
    prepareExampleGraph();
    visited = vector<bool>(graph.size(), false);

    bfs(0);

    return 0;
}
```

### Link do implementacji

{% embed url="https://ideone.com/fNxldF" %}
Przeszukiwanie grafu wszerz - BFS
{% endembed %}

### Implementation descriptioni

Funkcja `prepareExampleGraph` przygotowuje przyk??adowy graf w formie listy s??siedztwa zapisanej w dynamicznej tablicy typu `vector`. Przyk??adowy graf (przedstawiony tak??e na poni??szym rysunku) ma 7 wierzcho??k??w (numerowanych od zera) i jest nieskierowany.

Po utworzeniu przyk??adowego grafu (**linia 72**) przygotowujemy tablic?? `visited` i pocz??tkowo wype??niamy j?? warto??ciami `false` (**linia 73**). W tej tablicy zapami??tujemy dla ka??dego wierzcho??ka, czy zosta?? on ju?? odwiedzony, czy jeszcze nie. W tej implementacji korzystamy z dynamicznej tablicy typu `vector`, mo??na jednak r??wnie dobrze wykorzysta?? statyczn?? tablic?? (je??eli z g??ry znamy liczb?? wierzcho??k??w grafu).

Funkcja `bfs`  przyjmuje jeden parametr - numer (identyfikator, indeks) pocz??tkowego wierzcho??ka, od kt??rego chcemy zacz???? przeszukiwanie. Na pocz??tku tworzymy kolejk?? `nodes`, w kt??rej b??dziemy przechowywali kolejne wierzcho??ki do przetworzenia (**linia 48**). Pocz??tkowo do kolejki dodajemy tylko pierwszy wierzcho??ek, przekazany jako parametr funkcji (**linia 50**).

Nast??pnie przetwarzamy kolejne wierzcho??ki z kolejki, tak d??ugo jak w tej kolejce jest jeszcze co?? do przetworzenia (**linia 52**). W p??tli pobieramy pierwszy wierzcho??ek z kolejki (**linia 53**) i usuwamy go z kolejki (**linia 54**). Nast??pnie sprawdzamy, czy zosta?? ju?? wcze??niej odwiedzony, odwo??uj??c si?? do tablicy `visited` (**linia 55**). Je??eli wierzcho??ek zosta?? ju?? wcze??niej odwiedzony, to nie chcemy go ponownie przetwarza??, wi??c przechodzimy do kolejnego obrotu p??tli (**linia 56**).

Je??eli wierzcho??ek nie zosta?? jeszcze odwiedzony, to oznaczamy go jako odwiedzony (**linia 59**) i wypisujemy jego numer (**linia 60**). Nast??pnie  przechodzimy przez wszystkich s??siad??w aktualnie przetworzonego wierzcho??ka (**linia 62**). W pomocniczej zmiennej `next_node` zapami??tujemy numer przetwarzanego s??siada, pobranego z listy s??siedztwa (**linia 63**). Nast??pnie sprawdzamy, czy wierzcho??ek ten by?? ju?? odwiedzony (**linia 64**), a je??eli nie, to dodajemy go do kolejki (**linia 65**).

![Przyk??adowy graf wykorzystany w implementacji](../../../../.gitbook/assets/example_graph.png)

{% embed url="http://graphonline.ru/en/?graph=iyeQZmXVpPfZWqYG" %}
