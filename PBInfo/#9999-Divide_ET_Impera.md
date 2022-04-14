# Problema ???? - Divide ET Impera
```c++
#include "pch.h"
#include <iostream>

using namespace std;
#define DIMEN 1001

bool e_prim(int n);
int suma_divImp(int v[], int i, int s);
int exista_impar_divImp(int v[], int i, int s);
int suma_pare_divImp(int v[], int i, int s);
int exista_prime_divImp(int v[], int i, int s);
int cate_impare_divImp(int v[], int i, int s);
int toate_pare_divImp(int v[], int i, int s);
int maxim_prim_divImp(int v[], int i, int s);
int toate_egale_divImp(int v[], int i, int s);
int maxim_numar_divImp(int v[], int i, int s);

int main() {
	int n, v[DIMEN];
	cin >> n;
	for (int i = 1; i <= n; i++)
		cin >> v[i];
	// :D
	return 0;
}

int suma_divImp(int v[], int i, int s) {
	if (i == s)
		return v[s];
	int d1 = suma_divImp(v, i, (i + s) / 2);
	int d2 = suma_divImp(v, (i + s) / 2 + 1, s);
	return d1 + d2;
}

int exista_impar_divImp(int v[], int i, int s) {
	if (i == s) {
		if (v[s] % 2 == 1)
			return 1;
		return 0;
	}
	int d1 = exista_impar_divImp(v, i, (i + s) / 2);
	int d2 = exista_impar_divImp(v, (i + s) / 2 + 1, s);
	if (d1 || d2)
		return 1;
	return 0;
}

int suma_pare_divImp(int v[], int i, int s) {
	if (i == s) {
		if (v[s] % 2 == 0) return v[s];
		return 0;
	}
	int d1 = suma_pare_divImp(v, i, (i + s) / 2);
	int d2 = suma_pare_divImp(v, (i + s) / 2 + 1, s);
	return d1 + d2;
}

int exista_prime_divImp(int v[], int i, int s) {
	if (i == s) {
		if (e_prim(v[s]))	return 1;
	}
	int d1 = exista_prime_divImp(v, i, (i + s) / 2);
	int d2 = exista_prime_divImp(v, (i + s) / 2 + 1, s);
	if (d1 || d2) return 1;
	return 0;
}

bool e_prim(int n) {
	if (n < 2)	return false;
	if (n == 2)  return true;
	if (n % 2 == 0) return false;
	for (int d = 3; d * d <= n; d += 2)
		if (n % d == 0) return false;
	return true;
}

int cate_impare_divImp(int v[], int i, int s) {
	if (i == s) {
		if (v[s] % 2 == 1)
			return 1;
		return 0;
	}
	int d1 = cate_impare_divImp(v, i, (i + s) / 2);
	int d2 = cate_impare_divImp(v, (i + s) / 2 + 1, s);
	return d1 + d2;
}

int toate_pare_divImp(int v[], int i, int s) {
	if (i == s) {
		if (v[s] % 2 == 0)	return 1;
		return 0;
	}
	int d1 = toate_pare_divImp(v, i, (i + s) / 2);
	int d2 = toate_pare_divImp(v, (i + s) / 2 + 1, s);
	return d1 + d2;
}

int maxim_prim_divImp(int v[], int i, int s) {
	if (i == s) {
		if (e_prim(v[s])) return v[s];
		return 0;
	}
	int d1 = maxim_prim_divImp(v, i, (i + s) / 2);
	int d2 = maxim_prim_divImp(v, (i + s) / 2 + 1, s);
	if (d1 > d2)
		return d1;
	return d2;
}

int toate_egale_divImp(int v[], int i, int s) {
	if (i == s) {
		if (v[s] == v[1])	return 1;
		return 0;
	}
	int d1 = toate_egale_divImp(v, i, (i + s) / 2);
	int d2 = toate_egale_divImp(v, (i + s) / 2 + 1, s);
	return d1 + d2;
}
```
