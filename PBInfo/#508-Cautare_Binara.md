# Problema 508 - Cautare Binara
```c++
#include <iostream>

using namespace std;

int n, m;
int x[25001], y[200001];

int main() {

    cin >> n;
    for(int i = 1; i <= n; i++) cin >> x[i];
    cin >> m;
    for(int i = 1; i <= m; i++) cin >> y[i];
    int inceput, sfarsit, mijloc;
    for(int i = 1; i <= m; i++) {
        inceput = 1;
        sfarsit = n;
        while(inceput <= sfarsit) {
            mijloc = (inceput + sfarsit) / 2;
            if(x[mijloc] == y[i]) {
                cout << 1 << " ";
                break;
            }
            else {
                if(x[mijloc] < y[i])
                    inceput = mijloc + 1;
                else
                    sfarsit = mijloc - 1;
            }
        }
        if(inceput > sfarsit)
            cout << 0 << " ";
    }
    
    return 0;
}
```
