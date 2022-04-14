# Problema 547 - Numarare6
```c++
#include <iostream>

using namespace std;

int main() {
    int n, v[1001];
    
    cin >> n;
    for(int i=1;i<=n;i++)
        cin >> v[i];

    int maxim, minim, diferenta, cateEl=0;
    maxim = v[1];
    minim = v[1];

    for(int i=1;i<=n;i++) {
        if(v[i] > maxim)
            maxim = v[i];
        else if(v[i] < minim)
            minim = v[i];
    }

    diferenta = maxim - minim;
    for(int i=1;i<=n;i++) {
        if(v[i] == diferenta)   cateEl++;
    }
    
    cout << cateEl;

    return 0;
}
```
