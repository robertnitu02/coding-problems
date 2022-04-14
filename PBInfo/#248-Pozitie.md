# Problema 248 - Pozitie
```c++
#include <iostream>
#include <fstream>

using namespace std;

ifstream in("pozitie.in");
ofstream out("pozitie.out");


int main() {
    int n, v[10000], copie;
    in >> n;
    int k = 0;
    
    for(int i = 1; i <= n; i++) {
    	in >> v[i];    
        if(v[i] < v[1]) k++;
    }
    out << k+1;
    
    return 0;
}
```
