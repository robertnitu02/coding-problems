# Problema 451 - Calcul
```c++
#include <iostream>

using namespace std;

int main() {
	int n;
	
    cin >> n;
    if(n <= 15) {
		cout << n*n;
    }
    else if(16 <= n && n <= 30) {
    	int suma=0;
        
        while(n!=0) {
        	suma += n%10;
            n=n/10;
        }
        
        cout << suma;
    }
    else {
    	int p=1;
        
        while(n!=0){
        	p *= n % 10;
            n = n / 10;
        }
        
        cout << p;
    }
    
	return 0;
}
```
