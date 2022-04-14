# Problema 452 - cifimp
```c++
#include <iostream>

using namespace std;

int main() {
    int n, c, cifreImpare = 0;
    
    cin >> n;
    while(n!=0) {
		c = n % 10;
        if(c % 2 != 0)	cifreImpare++;
        n = n / 10;
    }
    cout << cifreImpare;
    
    return 0;
}
```
