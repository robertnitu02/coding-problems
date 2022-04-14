# Problema 7 - maxim2
```c++
#include <iostream>
#include <fstream>

using namespace std;

ifstream in("maxim.in");
ofstream out("maxim.out");

int Maxim(int nr1, int nr2) {
	if(nr1 > nr2)	return nr1;
    return nr2;
}

int main() {
    int a, b, maxim;
    
    in >> a >> b;
    maxim = Maxim(a, b);
    out << maxim;
    
    in.close();
    out.close();
	return 0;
}
```
