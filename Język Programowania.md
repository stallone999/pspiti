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
