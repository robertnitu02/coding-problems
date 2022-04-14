# Problema 355 - n minim
```c++
#include <iostream>

using namespace std;

int main() {
    int n, v[1001];
    
    cin >> n;
    for(int i=1;i<=n;i++)
        cin >> v[i];

    int MIN;
    MIN = v[1];
    for(int i=1;i<=n;i++) {
        if(MIN > v[i])
            MIN = v[i];
    }
    cout << MIN;
    
    return 0;
}
```
