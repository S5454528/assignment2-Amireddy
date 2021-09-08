# assignment2-Amireddy
# Sindhu Amireddy
###### Vietnam
I like Vietnam because of its beautiful beaches, **it’s culture**, amazing food (like pho), and friendly people. Vietnam is also famous for the Vietnam War, motorbikes (86% of households have one), Vietnamese coffee, __floating markets and rice terraces__.

---
### Maryville to Miami
1. We can travel from Maryville to Kansas city airport in 2 ways.
    1. By car
    2. By bus
2. Take a flight from kansas city to Miami.

* straw hat
* sunglasses
* cycling shoes

[link for AboutMe](https://github.com/S5454528/assignment2-Amireddy/blob/main/AboutMe.md)

---
### Foods that I recommend someone to try

The below table contains the Location and cost of the food and Drinks that I recommend

| Foods/Drinks | Location | cost |
|--------------|----------|------|
|Tandoori fish |Akash Miami|5$   |
|Baigan Bharta |Akash Miami|4$   |
|Pellegrino    |Akash Miami|3.5$ |
|Fuljar        |Akash Miami|4$   |

----
### Quotes of Life
> Seek respect, not attention. It lasts longerz. - *Ziad Abdelnour*

>You're Always One Choice Away from Changing Your Life. - *Mac Anderson*

----
### Code Fencing
> #### Spanning Tree
>A spanning tree is a subset of Graph G, which has all the vertices covered with minimum possible number of edges.
>[Link for Spanning Tree Definition](https://www.tutorialspoint.com/data_structures_algorithms/spanning_tree.htm)

```
struct Edge {
    int u, v, weight;
    bool operator<(Edge const& other) {
        return weight < other.weight;
    }
};

int n;
vector<Edge> edges;

int cost = 0;
vector<int> tree_id(n);
vector<Edge> result;
for (int i = 0; i < n; i++)
    tree_id[i] = i;

sort(edges.begin(), edges.end());

for (Edge e : edges) {
    if (tree_id[e.u] != tree_id[e.v]) {
        cost += e.weight;
        result.push_back(e);

        int old_id = tree_id[e.u], new_id = tree_id[e.v];
        for (int i = 0; i < n; i++) {
            if (tree_id[i] == old_id)
                tree_id[i] = new_id;
        }
    }
}
```
[Link for the above code](https://cp-algorithms.com/graph/mst_kruskal.html)
