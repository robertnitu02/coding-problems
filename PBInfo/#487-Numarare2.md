# Problema 487 - Numarare2
```c++
#include <iostream>

using namespace std;

int main() {
    int n, v[1001], suma = 0, Ma, C=0;
    
    cin >> n;
    for(int i=1;i<=n;i++) {
        cin >> v[i];
        suma += v[i];
    }
    Ma = suma / n;
    for(int i=1;i<=n;i++) {
        if(v[i] > Ma)   C++;
    }
    cout << C;
    
    return 0;
}
```
