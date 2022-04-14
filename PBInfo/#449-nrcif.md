# Problema 449 - nrcif
```c++
#include <iostream>

using namespace std;

int main() {
   int n, cateCifre=0;
   
   cin >> n;
   while(n!=0) {
      n = n / 10;
      cateCifre++;
   }
   cout << cateCifre;
    
    return 0;
}
```
