# Problema 456 - Piramida1
```c++
#include <iostream>
#include <math.h>

using namespace std;

int main() {
    int n, j = 1;
    char c;
    
    cin >> n >> c;
    while(j <= n) {
        for(int i = 1; i <= j; i++)
            cout << c;
        cout << endl;
        j++;
    }
    
    return 0;
}
```
