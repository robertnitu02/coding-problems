# Problema #1 - sum
``` c++
#include <iostream>
#include <fstream>

using namespace std;

ifstream in("sum.in");
ofstream out("sum.out");

int main() {

    int S = 0, a, b;
    in >> a >> b;
    
    S = a + b;
    out << S;
    
    in.close();
    out.close();
    
	return 0;    
}
```
