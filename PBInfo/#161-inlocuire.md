# Problema 161 - inlocuire
```c++
#include <iostream>

using namespace std;

int parte_intreaga(double n) {
    return int(n);
}

int main() {
    int n, v[1000], elNenule=0, sumaElNenule=0, Ma, k;

    cin >> n;
    for(int i=1;i<=n;i++)
        cin >> v[i];

    for(int i=1;i<=n;i++) {
        if(v[i] != 0) {
            elNenule++;
            sumaElNenule += v[i];
        }
    }

    Ma = sumaElNenule / elNenule;
    k = parte_intreaga(Ma);

    for(int i=1;i<=n;i++) {
        if(v[i] == 0)   v[i] = k;
    }

    for(int i=1;i<=n;i++)
        cout << v[i] << " ";

    return 0;
}
```
