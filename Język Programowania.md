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

## Ćwiczenie 7 - Program do oblicznia n-tego wyrazu w ciagu Fibonacciego

```c
#include <stdio.h>
int main (){
     int u1,u2,u3; // na kolejne wyrazy ciągu
     int n; // numer wyrazu
     int i; // licznik
     
     do {                                                   // pętla DO-WHILE - pętla wykona się conajmniej jeden raz, jeżeli podamy n<3 pętla się powtózy i poprosi o ponowne podanie liczby
         printf("Podaj numer wyrazu (co najmniej 3): ");
         scanf ("%d",&n);
         }
     while (n<3);
     u2=u1=1;  // podstawienie 1 z u2 i u1
     i=2;
     while (i++<n) {  // i++ zwiększ o 1 po użyciu, jeżeli warunek był prawdziwy wykonujemy pętle
            u3=u1+u2;
            u1=u2;
            u2=u3;
           }
//            for (i=3; I<=n; i++; u1=u2;u2=u3) u3=u1+u2;
            printf("Wyraz o numerze %d ma wartość %d", n,u3);
           
            getchar(); getchar();
            return 0;
     
     }
           
```
***

## Ćwiczenie 8 - Napisać program, który bedzie rysowal trójkat równoramienny zlożony z gwiazdek.

```c
#include <stdio.h>
#define znak '*'  // znak wypełnienia umieszczamy w pojedynczym apostrofie

int main (){
    int lbwier ; // całkowita liczba wierszy
    int lw; //licznik wierszy
    int lodst; // liczba odstępów poprzedzających gwiazdkę
    int j;
    
    printf("Ile wierszy?");
    scanf("%d",&lbwier);
    
    for (lw=0; lw <lbwier; lw++) {
        lodst=lbwier-lw-1;
        for(j=0; j<lodst; j++) putchar(' '); // funkcja która wyswietla na ekran pojedynczy znak
        for(j=0; j<2*lw+1; j++) putchar(znak); // funkcja wywswietlajaca gwizadki
        putchar ('\n'); // znak nowej lini \n 
        }
        getchar(); getchar();
    return 0;
}
```
***

#Ćwiczenie 9 - Zastosowanie petli FOR, WHILE, DO-WHILE.

```c
#include<stdio.h>

int main() {
    
    int n;
    
                                        // pętla for
    for (n=0;n<=23; n=n+1)
    printf("%d\n",n);
   
    putchar ('\n');
    getchar();
                             // pętla while
   
   n=0;
   while (n<=23) {
         printf("%d\n",n);
         n=n+1; 
         }
         putchar('\n');
        
        getchar();
          
 
                          //pętla DO - WHILE
  n=0;
  do {
        printf("%d\n",n);
        n=n+1;
        }while (n<=23);
                
       getchar();
       
    return 0;
}
```
***
