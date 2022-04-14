# Problema 1303 - Calculator
```c++
#include <iostream>

using namespace std;

int main() {
	int a, b, R;
    char operatie;
    
	cin >> a >> b >> operatie;
    
    switch(operatie) {
        case '+': {
        	R = a + b;
            
            cout << R;
            break;
        }
        case '-': {
        	if(a > b)
                R = a - b;
            else
                R = b - a;
            
            cout << R;
            break;
        }
        case '*': {
        	R = a * b;
            
            cout << R;
            break;
        }
        case '/': {
        	if(a > b)
                R = a / b;
            else
                R = b / a;
            
            cout << R;
            break;
        }
        default : cout << "Operatorul nu exista!";
    }
    
	return 0;
}
```
