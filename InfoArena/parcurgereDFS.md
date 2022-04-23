# Parcurgere DFS - componente conexe
```c++
	
#include <iostream>
#include <fstream>
#include <vector>
 
using namespace std;
#define NLIM 100005
 
ifstream in("dfs.in");
ofstream out("dfs.out");
 
int N, M, insule = 0;
bool Vizitat[NLIM];
vector < int > Muchii[NLIM];
 
void citire();
void afisare();
void dfs(int nod);
 
int main() {
    citire();
    afisare();
    dfs(1);
    out << insule;
    return 0;
}
 
void citire() {
    in >> N >> M;
    for(int i = 1; i <= M; i++) {
        int x, y;
        in >> x >> y;
        Muchii[x].push_back(y);
        Muchii[y].push_back(x);
    }
    in.close();
    for(int i = 1; i <= N; i++) Vizitat[i] = false;
}
 
void afisare() {
    for(int i = 1; i <= N; i++) {
        if(!Vizitat[i]) {
            insule++;
            dfs(i);
        }
    }
}
 
void dfs(int nod) {
    Vizitat[nod] = true;
    for(unsigned int i = 0; i < Muchii[nod].size(); i++) {
        int vecin = Muchii[nod][i];
        if(!Vizitat[vecin]) dfs(vecin);
    }
}
```