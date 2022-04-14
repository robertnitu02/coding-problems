# Problema 493 - Constr
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
    int n, y[205], x[205];
    
    cin >> n;
    for(int i = 1; i <= n; i++) {
        cin >> x[i];
        y[i] = x[i] % sum_cifre(x[i]);
    }
    for(int i = 1; i <= n; i++)
        cout << y[i] << " ";
        
    return 0;
}
```
