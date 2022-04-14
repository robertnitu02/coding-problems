# Problema 137 - Afisare Litere
```c++
#include <iostream>
#include <string.h>

using namespace std;

bool E(char alt[], char carac) {
    int i = 0;
    for(i = 0; i < strlen(alt); i++) {
        if(alt[i] == carac)
            return false;
    }
    return true;
}

int main() {
    char sir[256], alt[256];
    cin.get(sir, 256);
    int l = strlen(sir), k = 0;
    
    for(int i = 0; i < l; i++) {
        if(sir[i] >= 'a' && sir[i] <= 'z') {
            if(E(alt, sir[i])) {
                alt[k] = sir[i];
                k++;
            }
        }
    }
    alt[k] = '\0';
    l = strlen(alt);
    for(int i = 0; i < l; i++)
        cout << alt[i] << " ";
        
    return 0;
}
```
