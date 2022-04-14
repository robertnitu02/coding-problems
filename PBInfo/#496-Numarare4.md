# Problema 496 - Numarare4
```c++
#include <iostream>

using namespace std;

int cmmdc(int a, int b) {
    while(b != 0) {
        int r = a % b;
        a = b;
        b = r;
    }
    return a;
}

int main() {
    int n, v[205];
    
    cin >> n;
    for(int i = 1; i <= n; i++)
        cin >> v[i];
    int C = 0, ultim = v[n];
    for(int i = 1; i < n; i++)
        if(cmmdc(v[i], ultim) == 1)
            C++;
    cout << C;
    
    return 0;
}
```
