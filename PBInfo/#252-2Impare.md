# Problema 252 - 2Impare
```c++
#include <iostream>

using namespace std;

int main() {
    int n, prim_i, doi_i;
    cin >> n;
    int i = 1;
    while(i <= n) {
        if(i < n) {
            int aux = prim_i;
            prim_i = i;
            doi_i = aux;
        }
        i+=2;
    }
    cout << doi_i << " " << prim_i;
    return 0;
}
```
