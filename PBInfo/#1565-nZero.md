# Problema 1565 - nZero
```c++
#include <iostream>

using namespace std;

int main() {
    int n, a, p=1, P=1;
    const int numar = 10;

    cin >> n >> a;
    while(a != 0) {
        P = P * numar;
        a--;
    }

    p = n * P;
    cout << p;

    return 0;
}
```
