# Problema 498 - Numarare PIE
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
    int n, C = 0, v[205];
    
    cin >> n;
    for(int i = 1; i <= n; i++) cin >> v[i];
    for(int i = 1; i <= n; i++) {
        for(int j = i + 1; j <= n; j++) {
            if(cmmdc(v[i], v[j]) == 1)
                C++;
        }
    }
    cout << C;
    
    return 0;
}
```
