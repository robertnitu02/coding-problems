# Problema 405 - Suma Cifre Nr Prime
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

int cifre(int n) {
    int s = 0;
    while(n) {
        s += n % 10;
        n /= 10;
    }
    return s;
}

int main() {
    int n, s = 0;
    long int nr;
    
    cin >> n;
    while(n) {
        cin >> nr;
        if(prim(nr)) {
            s += cifre(nr);
        }
        n--;
    }
    cout << s;
    
    return 0;
}
```
