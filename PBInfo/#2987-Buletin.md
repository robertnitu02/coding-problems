# Problema 2987 - Buletin
```c++
#include <iostream>
#include <string.h>

using namespace std;

int main() {
    char sir[14];
    
    cin >> sir;
    for(int i = 1; i < 7; i+=2)
        cout << sir[i] << sir[i+1] << " ";
        
    return 0;
}
```
