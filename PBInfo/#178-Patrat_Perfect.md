# Problema 178 - Patrat Perfect
```c++
#include <iostream>
#include "math.h"

using namespace std;

int main() {
    int n, pp;
	cin >> n;
    
    pp = sqrt(n);
    if(pp*pp == n)
        cout << "da";
    else
        cout << "nu";
    
	return 0;
}
```
