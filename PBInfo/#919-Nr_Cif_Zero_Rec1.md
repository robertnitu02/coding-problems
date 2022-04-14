# Problema 919 - Nr Cif Zero Rec1
- doar functia
```c++
void nr_cif_zero(int n, int &nr) {
    if(n > 9) {
        nr_cif_zero(n/10, nr);
        if(n % 10 == 0) nr++;
    }else
        nr = !n;
}
```
