# Problema 822 - Nr Cif Zero Rec
- doar functia
```c++
int nr_cif_zero(int n) {
    if(n < 10 && n != 0)
        return 0;
    if(n == 0)
        return 1;
    else {
        if(n % 10 == 0)
            return (nr_cif_zero(n / 10) + 1);
        else
            return nr_cif_zero(n / 10);
    }
}
```
