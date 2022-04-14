# Problema 100 - NrApPrime
```c++
#include <iostream>
#include <fstream>

using namespace std;

ifstream in("nrapprime.in");
ofstream out("nrapprime.out");

bool prim(int n) {
    if(n < 2) return false;
    if(n == 2) return true;
    if(n % 2 == 0) return false;
    for(int d = 3; d * d <= n; d+=2)
        if(n%d==0)  return false;
    return true;
}

int main() {

    int n, v[101], elPrime=0;
    in >> n;

    for(int i=1;i<=n;i++) {
        in >> v[i];
        if(prim(v[i])) elPrime++;
    }

    out << elPrime;
    in.close();
    out.close();
    return 0;
}
```
