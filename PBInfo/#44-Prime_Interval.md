# Problema 44 - Prime Interval
```c++
#include <iostream>

using namespace std;

bool prim(int n) {
    if(n < 2) return false;
    if(n == 2) return true;
    if(n % 2 == 0) return false;
    for(int d = 3; d * d <= n; d+= 2)
        if(n % d == 0) return false;
    return true;
}

int main() {
    int a, b, c = 0;
    
    cin >> a >> b;
    if(a > b) {
        int aux = a;
        a = b;
        b = aux;
    }
    for(int i = a; i <= b; i++) {
        if(prim(i)) c++;
    }
    cout << c;
    
    return 0;
}
```
