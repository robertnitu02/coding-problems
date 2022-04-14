# Problema 509 - Ordonare
```c++
#include <iostream>

using namespace std;

int main() {
    int n, v[1001];
    
    cin >> n;
    for(int i=1;i<=n;i++)
        cin >> v[i];

    for(int i=1;i<=n;i++) {
        for(int j=i+1;j<=n;j++) {
            if(v[i] > v[j]) {
                int aux = v[i];
                v[i] = v[j];
                v[j] = aux;
            }
        }
    }

    for(int i=1;i<=n;i++)
        cout << v[i] << " ";

    return 0;
}
```
