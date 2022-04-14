# Problema 2288 - Cifra Impara Maxima
```c++
#include <iostream>

using namespace std;

int main() {
    int n, c, maximImp=0;
    cin >> n;

    while(n!=0) {
        c = n % 10;
        n = n / 10;
        if(c % 2 != 0) {
            if(c > maximImp) {
                maximImp = c;
            }
        }
    }

    if(maximImp > 0)
        cout << maximImp;
    else
        cout << "nu exista";

    return 0;
}
```
