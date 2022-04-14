# Problema 408 - Divizorii Oglinditului
```c++
#include <iostream>

using namespace std;

int main() {
    int n, inv=0, D=0;
    
    cin >> n;
    while(n!=0) {
        inv = inv * 10 + n % 10;
        n = n / 10;
    }

    for(int i=1;i<=inv;i++) {
        if(inv % i == 0)    D++;
    }
    cout << D;

    return 0;
}
```
