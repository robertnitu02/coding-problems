# Problema 347 - SumMaxMin
```c++
#include <iostream>

using namespace std;

int main() {
    int n, v[100], S=1;
    
    cin >> n;

    for(int i=1;i<=n;i++)
        cin >> v[i];

    int MIN, MAX;
    MIN = v[1];
    MAX = v[2];

    for(int i=1;i<=n;i++) {
        if(v[i] > MAX) MAX = v[i];
        if(v[i] < MIN)  MIN = v[i];
    }

    S = MIN + MAX;
    cout << S;

    return 0;
}
```
