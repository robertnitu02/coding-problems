# Problema 835 - Afisare Vector Rec
- doar functia
```c++
void afisvec(int v[], int n) {
    if(n != 0) {
        afisvec(v, n-1);
        cout << v[n-1] << " ";
    }
}
```
