# SHRUTHI CHINTHAKAYALA
## Salar Jung Museum
The **Salar Jung Museum** is an art museum located at Dar-ul-Shifa, on the southern bank of the Musi River in the city of **Hyderabad, Telangana, India.** It is one of the notable National Museums of India. Originally a private art collection of the Salar Jung family, it was endowed to the nation after the death of Salar Jung III. It was inaugurated on 16 December 1951. It has a collection of **sculptures, paintings, carvings, textiles, manuscripts, ceramics, metallic artifacts, carpets, clocks**, and furniture from Japan, China, Burma, Nepal, India, Persia, Egypt, Europe, and North America. It is one of the **largest museums in the world.**



---

# Directions from Rajiv Gandhi International Airport to Salar Jung Museum
1. Directions from airport to Museum
    1. Book a cab from RGI airport to Darulshifa, Hyderabad, Telangana
    2. take all ur belongings and book a cab to  which takes 20-30 min from airport
2. wait for the cab to arive 
    1. Sit back and enjoy the food and shopping centers at the airport 
    2. By listening to ur favourit music
3. Finally cab has arrived and you reached our location.


* Sight seeing places around museum:
 * Historical places:
    * Golkonda Fort
    * Charminar
    * Chowmahalla Palace
    * Mecca Masjid 
* Temples:
    * Birla Mandir
    * Jagannath temple
    * ISKON temple
* Parks  
    * Birla Planetarium
    * wonderla
    * KBR park

**[AboutMe.md](AboutMe.md)**

---

# 4 cities i  loved and i would love to suggest
I am going to create a table with  4 cities that I would love to recommend someone to visit = London, Sydney ,Paris , California.

|name of the city |locations to visit | duration|
|---|---|---|
|London|Buckingham Palace|30 minutes|
|Sydney|Opera House|45 minutes|
|Paris|Eiffel Tower|35 minutes|
|California|Yosemite National Park|75 minutes|

---
# Pithy Quote

> "When nobody else celebrates you, learn to celebrate yourself. When nobody else compliments you, then compliment yourself. It’s not up to other people to keep you encouraged. It’s up to you. Encouragement should come from the inside." *Jay Shetty*

<Br>
> “Lighten up, just enjoy life, smile more, laugh more, and don’t get so worked up about things.”  *Kenneth Branagh*

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

