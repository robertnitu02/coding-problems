# Problema 1453 - stergere1
```c++
#include <iostream>

using namespace std;

int main() {
    int n, v[1001];
    cin >> n;

    for(int i=1;i<=n;i++)
        cin >> v[i];

    for(int i=1;i<=n;i++) {
        if(v[i] % 2 != 0) {
           cout << v[i] << " ";
        }
    }

    return 0;
}
```
