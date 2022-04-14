# Problema 249 - PozitieX
```c++
#include <iostream>
#include <fstream>

using namespace std;

ifstream in("pozitiex.in");
ofstream out("pozitiex.out");

int main() {
    int n, x, v[10001], k = 0;
    bool exista = false;
    
    in >> x >> n;
    for(int i = 1; i <= n; i++) {
        in >> v[i];
        if(v[i] == x) exista = true;
        if(v[i] < x) k++;
    }
    if (exista == false) 
        out << "NU EXISTA";
    else 
        out << k+1;
    
    return 0;
}
```
