# assignment2-katta

# Harathi Katta
###### Ooty is my Favourite place.

***Ooty*** is located in *India* and is known as **Queen of Hill Stations**. It is one of the best place for exciting adventures like trekking, fishing,boating and camping. There are many places to see at that place.

---
#### Directions to Chicago
1. We can go by Airways or by Road.
2. Flight Jouney
    1. Start from Maryville to Kansas International Airport.
    2. Board the flight to Chicago
    3. we can reach Chicago in an hour.
3. By Road
    1. Go by car, we can use Maps and can go in 7 hours.
---
##### Items to take to my Favourite place
* Food
    * Snacks
    * Cool Drinks
* Mobile chargers
* Wallet

[Link of AboutMe.md](https://github.com/Harathikatta/assignment2-katta/blob/main/AboutMe.md)

---
#### Food Items Table

The Table contains information about the Food item, location available and its price. 

| S.No | Food Item | Location | Price |
| --- | --- | --- | ---: |
| 1 | CFA | Chich Fil-A | $4.80 |
| 2 | Spicy | Chich Fil-A | $4.80 |
| 3 | Fries | Chich Fil-A | $6.00 |
| 4 | nuggets | Chich Fil-A | $5.80 |

---
### My Favourite Quotes
>Be the kind of a girl people read books about. *~Keerthana*<br>     
>And now that you dont have to be perfect, you can be good.*~John Steinbeck*

---
#### Code Fencing
> ### Spanning Tree: <br>
> A spanning tree is a subset of Graph G, which has all the vertices covered with minimum possible number of edges.
[Definition Link](https://www.tutorialspoint.com/data_structures_algorithms/spanning_tree.htm)
```
int n;
vector<vector<int>> adj; // adjacency matrix of graph
const int INF = 1000000000; // weight INF means there is no edge
struct Edge {
    int w = INF, to = -1;
};
void prim() {
    int total_weight = 0;
    vector<bool> selected(n, false); vector<Edge> min_e(n);
    min_e[0].w = 0;
    for (int i=0; i<n; ++i) {
        int v = -1;
        for (int j = 0; j < n; ++j) {
            if (!selected[j] && (v == -1 || min_e[j].w < min_e[v].w))
                v = j; }
        if (min_e[v].w == INF) {
            cout << "No MST!" << endl;exit(0);s}
        selected[v] = true; total_weight += min_e[v].w;
        if (min_e[v].to != -1)
            cout << v << " " << min_e[v].to << endl;
        for (int to = 0; to < n; ++to) {
            if (adj[v][to] < min_e[to].w)
                min_e[to] = {adj[v][to], v};
        }
    }
    cout << total_weight << endl;
}
```
[The code is from the link](https://cp-algorithms.com/graph/mst_prim.html)




