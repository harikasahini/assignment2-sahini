# assignment2-sahini
Repository for assignment 2
# HARIKA SAHINI
## Zodiac grill restaurant
 The entire restaurant is decorated with **Zodiac signs** and the sitting arrangement was superb.<br> Moreover, the best thing about the restaurant is its **Multi-national cuisines**.

 ---

 ### Directions for Zodiac grill restaurant
 1. Hyderabad airport is closest airport to the Zodiac grill restaurant.
 2. Take a cab from airport to the Kukatpally main road.
 3. Get down at Metro station on main road .
 4. The restaurant will be opposite to the Metro station.
 ### Recommended food items
 * Grilled Salamon dish
 * Mughalai Biryani
 * Banana Split Ice Cream
 * Manchow Soup<br>
 [Link for details about me](https://github.com/harikasahini/assignment2-sahini/blob/main/AboutMe.md)

 ---

 # Sports Table
Regular sporting activities can prevent chronic diseases and help develop healthy heart, strong bones, and enhanced lung function. Below are some of the sports which can help people to maintain healthy lifestyle. The table below shows the location where the sport can be played and the amount required for the initial equipment needed.

| Activity name | Location | Amount in USD($) |
| --- | --- | ---: |
| Badminton | Recreation Centre | 100 |
| Cricket | Filed's house | 200 |
| Squash | Hower stadium | 200 |
| Tennis | Spring court | 150 |

---

# Quotes I like

>Talk to yourself once in a day, otherwise you may miss meeting an intelligent person in this world. -*Swami Vivekananda*

>It's OK to have your eggs in one basket as long as you control what happens to that basket. -*Elon musk*

---

# Prim's Algorithm

>Kruskal’s Algorithm finds the Minimum Spanning Tree of a graph by starting with one of the edges with minimum weight and then trying to include the next minimum-weight edge from the rest of the edges while avoiding formation of any cycles.<br>
<https://efficientcodeblog.wordpress.com/2017/12/11/kruskals-algorithm-implementation/>

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
<https://cp-algorithms.com/graph/mst_kruskal.html>