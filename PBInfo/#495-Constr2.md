# Problema 495 - Constr2
```c++
#include <iostream>

using namespace std;

bool prim(int n) {
    if(n < 2)
        return false;
    if(n == 2)
        return true;
    if(n % 2 == 0)
        return false;
    for(int d = 3; d * d <= n; d+=2)
        if(n % d == 0)
            return false;
    return true;
}

int main() {
    int n, v[205];
    
    cin >> n;
    for(int i = 1; i <= n; i++)
        cin >> v[i];
    for(int i = n; i >= 1; i--)
        if(prim(v[i])) cout << v[i] << " ";
        
    return 0;
}

```
