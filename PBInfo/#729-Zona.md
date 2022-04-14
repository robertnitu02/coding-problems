# Problema 729 - Zona
```c++
#include <iostream>

using namespace std;
int n, mat[205][205];
int valori[205], poz;

bool apare(int poz, int v[], int x) {
    for(int i = 1; i <= poz; i++)
        if(x == v[i]) return false;
    return true;
}

void sortare() {
    for(int i = 1; i <= poz; i++) {
        for(int j = i + 1; j <= poz; j++) {
            if(valori[i] > valori[j]) {
                int aux = valori[i];
                valori[i] = valori[j];
                valori[j] = aux;
            }
        }
    }
}

int main() {

    cin >> n;
    for(int i = 1; i <= n; i++)
        for(int j = 1; j <= n; j++)
            cin >> mat[i][j];
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= n; j++) {
            if(i > j && i + j < n + 1) {
                if(apare(poz, valori, mat[i][j])) {
                    poz++;
                    valori[poz] = mat[i][j];
                }
            }
        }
    }
    sortare();
    for(int i = 1; i <= poz; i++)
        cout << valori[i] << " ";
      
    return 0;
}
```
