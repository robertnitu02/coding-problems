# Problema 87 - Lungime Maxima
```c++
#include <iostream>
#include <string.h>
#include <fstream>

using namespace std;

ifstream in("lgmax.in");
ofstream out("lgmax.out");

int main() {
    int n, maxim = 0, coeficient = 0, MAX;
    char sir[100][256];
    
    in >> n;
    while(n) {
        in.get();
        in.get(sir[coeficient], 256);
        if(strlen(sir[coeficient]) > maxim) {
            maxim = strlen(sir[coeficient]);
            MAX = coeficient;
        }
        coeficient++;
        n--;
    }
    out << sir[MAX];
    
    in.close();
    out.close();
    return 0;
}
```
