# Problema 354 - n maxim
```c++
#include <iostream>

using namespace std;

int main() {
    int n, v[1001];
    
    cin >> n;
    for(int i=1;i<=n;i++)
        cin >> v[i];
    int MAX;
    MAX = v[1];
    for(int i=1;i<=n;i++) {
        if(MAX < v[i])
            MAX = v[i];
    }
    cout << MAX;

    return 0;
}
```
