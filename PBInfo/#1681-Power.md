# Problema 1681 - Power
```c++
#include <iostream>

using namespace std;

int main() {
    int a, b, P=1;
    cin >> a >> b;

    while(b != 0) {
        P *= a;
        b--;
    }

    cout << P;

    return 0;
}
```
