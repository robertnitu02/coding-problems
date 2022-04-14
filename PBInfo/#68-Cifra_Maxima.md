# Problema 68 - Cifra Maxima
```c++
#include <iostream>

using namespace std;

int main() {
    int n, c_max = 0;
    
    cin >> n;
    while(n) {
        int cifra = n % 10;
        if(cifra > c_max)   c_max = cifra;
        n /= 10;
    }
    cout << c_max;
    
    return 0;
}
```
