# Problema 351 - Piramida
```c++
#include <iostream>
#include <math.h>

using namespace std;

int main() {
    int n, j = 1;
    
    cin >> n;
    while(j <= n) {
        for(int i = 1; i <= j; i++)
            cout << i << " ";
        cout << endl;
        j++;
    }
    
    return 0;
}
```
