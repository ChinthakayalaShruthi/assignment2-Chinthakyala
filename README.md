# SHRUTHI CHINTHAKAYALA
## Salar Jung Museum
The **Salar Jung Museum** is an art museum located at Dar-ul-Shifa, on the southern bank of the Musi River in the city of **Hyderabad, Telangana, India.** It is one of the notable National Museums of India. Originally a private art collection of the Salar Jung family, it was endowed to the nation after the death of Salar Jung III. It was inaugurated on 16 December 1951. It has a collection of **sculptures, paintings, carvings, textiles, manuscripts, ceramics, metallic artifacts, carpets, clocks**, and furniture from Japan, China, Burma, Nepal, India, Persia, Egypt, Europe, and North America. It is one of the **largest museums in the world.**



---

# Directions from Rajiv Gandhi International Airport to Salar Jung Museum
1. Catch a directions of 1,396 miles from marryville to Henderson via flight
2. catch a cab and go to the kansas airport(mca)
    1. take a flight from kansas to lasvegas airport(las)
    2. take all ur belongings and book a cab to henderson which takes 10-15 min from airport
3. wait for the cab to arive 
    1. Sit back and enjoy the lightning and mountain view 
    2. By listening to ur favourit music
4. Finally we have reached our location yeyeye..!!


* Sight seeing places around museum:
 * Drinks:
    * Cocola
    * Tropicana
    * Minute maid
    * Water 
* Accessories:
    * Airpods
    * iwatch
    * DSLR
    * Power Bank  
    * Cable 
* Snacks  
    * Chocolates
    * Chips

**[AboutMe.md](AboutMe.md)**

---

# food i loved and i would love to suggest
I am going to create a table with  4 food items that I would love to recommend someone try = Thai Friedrice, Pizza,Sushi , Icecream.

|Food Item|Location| Cost|
|---|---|---|
|Thai Friedrice|rewoke|10$|
|Pizza|Pizzeria|7$|
|Sushi|Republica|12$|
|Icecream|creamworld|2$|


# Pithy Quote

> "When nobody else celebrates you, learn to celebrate yourself. When nobody else compliments you, then compliment yourself. It’s not up to other people to keep you encouraged. It’s up to you. Encouragement should come from the inside." *Jay Shetty*
<Br>
> "Hell is empty and all the devils are here." *William Shakespeare*


---
# Dijkstra Algorithm
> Dijkstra's algorithm is an algorithm for finding the shortest paths between nodes in a graph, which may represent, for example, road networks. It was conceived by computer scientist Edsger W. Dijkstra in 1956 and published three years later. The algorithm exists in many variant

[Click Here to Know More](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm)


```

const int INF = 1000000000;
vector<vector<pair<int, int>>> adj;

void dijkstra(int s, vector<int> & d, vector<int> & p) {
    int n = adj.size();
    d.assign(n, INF);
    p.assign(n, -1);
    vector<bool> u(n, false);

    d[s] = 0;
    for (int i = 0; i < n; i++) {
        int v = -1;
        for (int j = 0; j < n; j++) {
            if (!u[j] && (v == -1 || d[j] < d[v]))
                v = j;
        }

        if (d[v] == INF)
            break;

        u[v] = true;
        for (auto edge : adj[v]) {
            int to = edge.first;
            int len = edge.second;

            if (d[v] + len < d[to]) {
                d[to] = d[v] + len;
                p[to] = v;
            }
        }
    }
}
```
[code source](https://cp-algorithms.com/graph/dijkstra.html)

