# Problema 794 - Serpuire
```c++
#include <iostream>

using namespace std;

int main() {
    int n, mat[30][30];
    
    cin >> n;
    for(int i = 1; i <= n; i++)
        for(int j = 1; j <= n; j++)
            cin >> mat[i][j];
    int i, j, k;
    i = 0;
    for(k = 1; k <= 2 * n - 1; k++) {
        if(k > n)
            i++;
        if(k % 2 == 0)
            for(j = k - i; j > i; j--)
                cout << mat[j][k+1-j] << " ";
        else
            for(j=i+1; j<=k-i; j++)
                cout << mat[j][k+1-j] << " ";
    }
    
    return 0;
}
```
