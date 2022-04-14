# Problema 375 - Urmatorul Prim
```c++
#include <iostream>
#include <cmath>

using namespace std;

int main() {
    int n;
    
    cin>>n;
    if (n == 1) {
        cout<<2;
        return 0;
    }
    if(n % 2 == 0)
        n++;
    else
        n += 2;

    while(true) {
        if(n > 1 && (n % 2 != 0 || n == 2)) {
            int sq = sqrt(n), d;
            for(d = 3; d <= sq; d += 2) {
                if(n % d == 0)
                    break;
            }
            if(d > sq)
                break;
        }
        n += 2;
    }
        
    cout<<n;
}
```
