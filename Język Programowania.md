#Wyklady z Jezyka Programowania

###Sobota 02.03.2013 godz. 8.30               

## Podstawowy szkielet programu w C++ - Ćwiczenie pierwsze

```c
#include <stdio.h> // .h - rozszerzenie plika naglówkowego  

int main () {
    int a,b;
    a=3;
    b=7;
    printf("Wynik mnozenia to %d", a*b);
    getchar();  // pobierz znak z klawiatury
    return 0;
}
```   
***

## Ćwiczenie 2 - dodawanie, odejmowanie i dzielenie

```c
#include <stdio.h>

int main () {
    int a,b;
    a=3;
    b=7;
    printf("%d*%d=%d\n",a,b,a*b); // wyświetla koljeny argument, który jest liczbą całkowitą, a,b oraz wynik mnożenia tych liczb
    printf("%d+%d=%d\n",a,b,a+b);
    printf("%d-%d=%d\n",a,b,a-b);
    printf("%d/%d=%d",a,b,a/b);
    getchar();
    return 0;
}
```
***

## Ćwiczenie 3 - argument zmienno przecinkowy "lf", wykorzystanie "double"

```c
#include <stdio.h>

int main () {
    double a,b;
    a=3.0;
    b=7.0;
    printf("%lf * %lf=%lf\n",a,b,a*b); // wyświetla koljeny argument, który jest liczbą całkowitą, a,b oraz wynik mnożenia tych liczb
    printf("%lf + %lf=%lf\n",a,b,a+b);
    printf("%lf - %lf=%lf\n",a,b,a-b);
    printf("%lf / %lf=%lf",a,b,a/b); // lf- liczba zmienno przecinkowa, do 6 miejsc po przecinku , float- pamiętany w 4bajtach, double-8bajtów, 

    getchar();
    return 0;
}
```
***

## Ćwiczenie 4 - ograniczenie wyswietlanych miejsc po przecinku

```c
#include <stdio.h>

int main () {
    double a,b;
    a=3.0;
    b=7.0;
    printf("%.0lf * %.0lf =%.0lf\n",a,b,a*b); // .0lf - wyświetla zero miejsc po przecinku
    printf("%.0lf + %.0lf =%.0lf\n",a,b,a+b);
    printf("%.0lf - %.0lf =%.0lf\n",a,b,a-b);
    printf("%.0lf / %.0lf =%.3lf",a,b,a/b); // lf- liczba zmienno przecinkowa, do 6 miejsc po przecinku , float- pamiętany w 4bajtach, double-8bajtów, 

    getchar();
    return 0;
}
```
***

## Ćwiczenie 5 - Oblicz pole i obwód kola z użyciem plika naglówkowego <math.h>

```c
#include <stdio.h>
#include <math.h>
int main () {
    double r;
    //const double pi=3,1415926;          //stały, M_PI zadeklarowane w pliku <math.h>
    printf("Podaj promien kola: ");
    scanf("%lf",&r);
    printf("Pole kola o promieniu %.0lf wynosi %lf\n",r,M_PI*r*r);
    printf("Obowd kola wynosi: %d * %lf * %lf = %lf ",2,M_PI,r, 2*M_PI*r );
    getchar(); getchar ();
    return 0;
}
```
***

**scanf** - wczytaj z klawiatury ***(%fl- liczbe typu double)***, wszystkie zmienne poprzedzamy *&*
<br> Potęgowanie w języku c++ nie można pisać **daszka**, trzeba rozpisywać za pomocą * czyli mnożenia

***

## Ćwiczenie 6 - Przeliczanie stopni z Faranheita na Celsiusza.

```c
#include <stdio.h>

int main () {
    double fahr, celsius;
    int lower, upper, step; 
    lower=0;
    upper=300; // instrukcje podstawienia 
    step=20;
    fahr=lower; // za wartość zmiennej fahr podstaw lower
while (fahr<=upper){             // while - dopuki
      celsius=5*(fahr-32)/9;  // w C++ działania wykonywane są od lewej do prawej np a+b*c/d to najpierw wykonane będzie mnożenie następnie dzielenie a dopiero wtedy dodawanie                              
      printf("%.3lf\t %.3lf\n",fahr, celsius); // /t - tabulatora // %5.1lf - liczba ma być wyświetlona "wielkość pola.ilość miejsc po przecinku"
      fahr=fahr+step; // za fahr podstaw step
} 
getchar();
return 0;
}
```
***

## Ćwiczenie 7 - Preprocesor DEFINE i petla FOR

```c
#include <stdio.h>
#define LOWER 0  // define - stałe preprocesora języka C, nie stawiamy średników, pełni funkcję znajdź i zamień
#define UPPER 300
#define STEP 20

int main () {
    int fahr;
    for (fahr=LOWER;fahr<=UPPER;fahr=fahr+STEP) // zmienne odzielamy średnikiem, za instrukcją FOR nie stawiamy średnika
    printf("%3d %6.1lf\n",fahr,(5.0/9.0)*(fahr-32));
    getchar();
    return 0;
}
```
***
