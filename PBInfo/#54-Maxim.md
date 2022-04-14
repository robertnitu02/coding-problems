# Problema 54 - Maxim
```c++
#include <iostream>

using namespace std;

int main() {
    int n, MAX;

    MAX = -2;
    cin >> n;
    if(n == 0)
        cout << "NU EXISTA";
    else {
        while(n != 0) {
            cin >> n;
            if(n > MAX)   MAX = n;
        }
        cout << MAX;
    }

    return 0;
}
```
