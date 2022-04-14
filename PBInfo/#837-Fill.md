# Problema 837 - Fill
```c++
#include <fstream>
#include <iostream>

using namespace std;

ifstream in("fill.in");
ofstream out("fill.out");

int n, m, matrice[101][101], matriceFill[101][101];
int numar_zona;
int di[4] = {0, 0, -1, 1};
int dj[4] = {1, -1, 0, 0};

bool OK(int i, int j) {
    if(i < 1 || j < 1 || i > n || j > m) return false;
    if(matriceFill[i][j]) return false;
    if(matrice[i][j] == 0) return false;
    return true;
}

void algFill(int i, int j) {
    matriceFill[i][j] = numar_zona;
    for(int d = 0; d < 4; d++) {
        int i_urmator = i + di[d];
        int j_urmator = j + dj[d];
        if(OK(i_urmator, j_urmator) && matrice[i_urmator][j_urmator] == matrice[i][j])
            algFill(i_urmator, j_urmator);
    }
}

int main() {
    in >> n >> m;
    for(int i = 1; i <= n; i++)
        for(int j = 1; j <= m; j++)
            in >> matrice[i][j];
    in.close();
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= m; j++) {
            if(!matriceFill[i][j]) {
                if(matrice[i][j] == 1) numar_zona++;
                algFill(i, j);
            }
        }
    }
    out << numar_zona;
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= m; j++)
            cout << matriceFill[i][j] << " ";
        cout << endl;
    }
    return 0;
}
```
