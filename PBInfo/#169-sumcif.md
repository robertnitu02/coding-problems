# Problema 169 - sumcif
```c++
#include <iostream>

using namespace std;

int main() {
    int n, s=0;
    cin >> n;
    
    while(n) {
    	  s = s + n % 10;
        n = n / 10;
    }
    cout << s;
    
	return 0;    
}
```
