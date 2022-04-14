# Problema 46 - Suma Pare
```c++
#include <iostream>

using namespace std;

int main() {
    int n, S=0;
    
    cin >> n;
    for(int i=1;i<=n*2;i++) {
  		if(i%2==0)	
  		    S+=i;
    }
    cout << "Suma este " << S;
    
	return 0;
}
```
