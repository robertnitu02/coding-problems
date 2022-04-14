# Problema 469 - Interval2
```c++
#include <iostream>

using namespace std;

int main() {
    int a, b, x;
    cin >> a >> b >> x;
    
    // [a;b] -->  x <= a si b <= x
    if(a <= x && x <= b) 
        cout << "DA";
    else
        cout << "NU";
    
	return 0;    
}
```
