# Problema 499
```c++
#include <iostream>

using namespace std;

int sum_cifre(int n) {
    int s = 0;
    while(n) {
        s += n % 10;
        n = n / 10;
    }
    return s;
}

int main() {
    int n, C = 0, v[205];
    
    cin >> n;
    for(int i = 1; i <= n; i++) cin >> v[i];
    for(int i = 1; i <= n; i++) {
        for(int j = i + 1; j <= n; j++) {
            if(sum_cifre(v[i]) == sum_cifre(v[j]))
                C++;
        }
    }
    cout << C;
    
    return 0;
}

```
