# Problema 278 - MaxMin1
```c++
#include <iostream>

using namespace std;

int n, m, v[105], x[105];

bool f(int a) {
    for(int i = 1; i <= m; i++)
        if(a <= x[i]) return false;
    return true;
}

int main() {

    cin >> n;
    for(int i = 1; i <= n; i++)
        cin >> v[i];
    cin >> m;
    for(int i = 1; i <= m; i++)
        cin >> x[i];
    int C = 0;
    for(int i = 1; i <= n; i++)
        if(f(v[i])) C++;
    cout << C;
    
    return 0;
}
```
