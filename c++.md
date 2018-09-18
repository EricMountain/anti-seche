# C++

``` c++
#include <iostream>
#include <string>
#include <vector>
#include <algorithm>
#include <map>
#include <time.h>
#include <queue>

using namespace std;

int main() {
  int width;
  cin >> width; cin.ignore();
  
  string line;
  getline(cin, line);
  
  // Iteration
  std::vector<int> v = …;
  for(std::vector<int>::const_iterator it = v.begin(); it != v.end(); ++it) {
    v.erase(it);
    
    if (std::find(path.begin(), path.end(), it) != path.end()) {
      …
     }
  }
  
  // Pair
  std::pair<int,int> p = std::make_pair(a, b);
  p.first …
  p.second …
  
  // Append to Vector
  std::vector<int> visitedNodes;
  visitedNodes.push_back(nodeIndex);
 
  // Priority queue
  std::priority_queue<std::pair<int,int>, std::vector<std::pair<int,int> >, std::greater<std::pair<int,int> > > pq;
  for(std::vector<int>::iterator it = neighbours.begin(); it != neighbours.end(); ++it) {
    pq.push(std::make_pair(value, *it));
  }

  while (!pq.empty()) {
    std::pair<int,int> item = pq.top();
    pq.pop();
    if (item.second == …) {
      continue;
    }
  }

  // Init map entry if key missing
  std::map<int, std::vector<int> > rel;
  if (rel.find(something) == rel.end()) {
    rel[something] = std::vector<int>();
  }
}

long getmillis()
{
    struct timespec tv;
    clock_gettime(CLOCK_MONOTONIC, &tv);
    long millis = tv.tv_nsec;
    millis /= 1000000;
    millis += (tv.tv_sec * 1000);
    return millis;
}

class Whatever {
  int id;
  bool isExit;
  
  public:
  Node() : id(0), isExit(false) { }
  int getId() { return id; }
}

int Whatever::doSomething() {
  return this;
}
```
