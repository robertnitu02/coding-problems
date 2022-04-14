# Problema 209 - ElimCif
```c++
#include <iostream>

using namespace std;

int main() {
    int n, cifra;
    cin >> n;
    
    cifra = (n/100)*10+n%10;
    cout << cifra;
    
	return 0;    
}
```
