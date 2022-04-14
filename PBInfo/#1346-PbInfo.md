# Problema 1346 - PbInfo
```c++
#include <iostream>
#include <string.h>
#include <fstream>

using namespace std;

ifstream in("pbinfo.in");
ofstream out("pbinfo.out");

int main() {
    char sir_link[101], cuvinte[100][103];
    in.get();
    in.get(sir_link, 101);
    int n, k = 0;
    in >> n;
    while(n) {
        in.get();
        in.get(cuvinte[k], 103);
        k++;
        n--;
    }
    if(strstr(sir_link, "virus"))
        out << "DA";
    else {
        bool E =  false;
        for(int i = 0; i < k; i++) {
            if(strstr(sir_link, cuvinte[i])) {
                E = true;
                break;
            }
        }
        if(E)
            out << "DA";
        else
            out << "NU";
    }
    in.close();
    out.close();
    return 0;
}
```
