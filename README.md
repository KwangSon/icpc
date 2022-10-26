# icpc

## Keep in mind
0. 급하게 하면 '절대' 안된다. (시간을 더 써서라도 침착해야한다.)
1. 컴파일이 되어야하는지, 복잡도 정리도 요하는지. 맞느 알고리즘인지 확인해주는지. 힌트느 주는지.
2. 구현보다는 생각으로 먼저 정리하자
3. clean code (STL, auto, reference)
4. test

## How to solve
0. brute-force로 안되는 것은 어차피 잘 모르는 것이다.
1. 비슷한 유형을 대입해본다.
2. 중복 제거.

## types
1. Brute-force, greedy
2. Sub-problem(D&Q, dynamic, combination)
3. math, bit-mask
4. string
5. graph

# cheet sheet

## vector
### Initialize
```
vector<int> vect(n); // just size
vector<int> vect(n, 10); // size with value
vector<int> vect{ 10, 20, 30 }; // specific value
vector<int> vect = { 10, 20, 30 }; // specific value 2
```

## queue
```
#include <queue>
queue<int> q;
q.push() // think it is push_back, q.pop() // delete from front, q.front(), q.back()
```

## priority_queue
```
#include <queue>
priority_queue<int> pq;
pq.push(), pq.pop(), pq.top()
```
### cmp
```
struct Student {
    int id;
    int math, eng;
    bool operator<(const Student s) const {
        return this->id > s.id;
    }
};
```

## unordered_map
### Initialize
```
#include <unordered_map>

unordered_map<Key, value> umap = {{K,V}, {K,V} ...};
```
### Usage
```
umap[K] = V;
cout << umap[K] << endl;
// If umap[K] value not exist. just return basic value (e.g. int -> 0, string -> null)
// use find or contains
if(umap.contains(x))

auto search = example.find(x);
if (search != example.end()) { // found
```
## sort
```
sort(vec.begin(), vec.end());

bool compare(int i, int j) { return i > j; }
sort(vec.begin(), vec.end(), compare);
```

## binary seaerch
```
// must sorted before.
lower_bound(arr, arr + 6, 6)

lower_bound // return SAME or greater
upper_bound // return greater
```

## graph path
### Dijkstra Algorithm
```
O((V+E)lgV)
dist[V] ..
use priority_queue to get shortest dist[V].
```
