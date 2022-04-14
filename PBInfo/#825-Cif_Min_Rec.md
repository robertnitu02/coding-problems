# Problema 825 - Cif Min Rec
- doar functia
```c++
int cifmin(int n) {
    if(n <= 9) return n;
    int m = cifmin(n / 10);
    if(n % 10 < m)
        return n % 10;
    return m;
}
```
