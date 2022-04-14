# Problema 824 - Cif Max Rec
- doar functia
```c++
int cifmax(int n) {
    if(n <= 9) 
        return n;
    int m = cifmax(n / 10);
    if(m > n % 10)
        return m;
    return n % 10;
} 
```
