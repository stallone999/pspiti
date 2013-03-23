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
## Ćwiczenie 10 na srednia arytmetyczna

```c
# include <stdio.h>  // instrukcja preproceosra
int main () {
int n, i;
double x, suma=0.0, srednia;
do {                                                            // poczatek pierwszej petli
    printf ("Podaj ilosc liczb (co najmniej 1): ");
    scanf ("%d", &n);
}
while(n<1);              // koniec pierwszej petli
for(i=1;i<=n;i++) {                 // poczatek petli for
printf("Podaj %d liczbe:", i);
scanf("%lf", &x);
suma=suma+x;
}                                   // koniec petli for
    srednia = suma/n;
    printf("Suma podanych %d liczb wynosi: %.3lf \n", n, suma);
    printf("Srednia z podanych %d liczb wynosi: %.3lf", n,srednia);
    getchar();
    getchar();
    return 0;
}
```
***
## Ćwiczenie 11 - Wypisz kwadraty i szeciany liczb naturalnych od 1 do liczby podanej przez użytkownika za pomoca petli for, while, do-while.

```c
#include <stdio.h>
int main() {
int i, n;
    printf("Podaj liczbe:");
    scanf("%d", &n);
    for(i=1;i<=n;i++) {                         /*Pętla for*/
    printf("%d,kwadraty:%d\t,szesciany:%d\t \n", i, i*i, i*i*i);
    }

    printf("\n");                               /*oddzielenie wyników*/

    i=1;                                        /*Pętla while*/
    while(i<=n) {
    printf("%d,kwadraty:%d\t,szesciany:%d\t \n", i, i*i, i*i*i);
    i++;
    }

    printf("\n");                               /*oddzielenie wyników*/

    i=1;                                        /*Pętla do-while*/
    do  {
    printf("%d,kwadraty:%d\t,szesciany:%d\t \n", i, i*i, i*i*i);
    i++;
        }
    while(i<=n);
    getchar();
    getchar();
    return 0;
}
```
***

## Ćwiczenie 12 - Oblicz za pomoca petli for i while sume kwadratow liczb od 3 do 15.

```c
#include <stdio.h>
int main() {
int i, suma=0;
    for(i=3;i<=15;i++) {    /*Pętla for*/
        suma=suma+(i*i);
    }
    printf("%d \n",suma);

    printf("\n");       /*Rozdzielenie wyników */


    i=3;            /*Pętla while; w tym miejscu ustawiamy i */
    suma=0;         /*wyzerowanie sumy, ponieważ nie jest już =0*/
    while(i<=15)    {
    suma=suma+(i*i);
    i++;
    }
    printf("%d \n",suma);
    getchar();
    return 0;
}
```
***

## Ćwiczenie 13 - Wypisz sinusy i cosinusy katów 0...180 stopni z krokiem co 30 stopni za pomoca petli for.

```c
#include <stdio.h>
#include <math.h>
int main() {
    double x;
    
  printf ("Zadanie wykonane w petli FOR:\n\n");
  
    for (x=0;x<=180;x=x+30) {
        printf("sin(%.0lf)= %lf \n",x,sin(x*M_PI/180));
        printf("cos(%.0lf)= %lf \n\n",x ,cos(x*M_PI/180));
}

printf ("Zadanie wykonane w petli do-while:\n\n");

x=0;
do {
    printf("sin(%.0lf)= %lf \n",x,sin(x*M_PI/180));
    printf("cos(%.0lf)= %lf \n\n",x ,cos(x*M_PI/180));
    x=x+30;
}
while (x<=180);

getchar();
return 0;
}
```
***

## Ćwiczenie 14 - Wypisz znaki od 'a' do 'k' wraz z ich kodami ASCII (dziesietnie, szesnatkowo) w kolejnosci rosnacej i malejacej za pomoca petli FOR.

```c
#include <stdio.h>
int main () {
    char i;
    for (i='a'; i<='k'; i++) {
        printf ("Litera:%c, znak ASCII:%3d, szesnastkowo: %2x\n",i,i,i); // %c - wyświetla jako litera, %3d - w kodzie ASCII, %2x - w kodzie szesnastkowym
        }
        getchar();
        return 0;
}
    
```
***

## Ćwiczenie 15 - Napisz petle WHILE wypisujaca na ekran znaki podane przez uzytkownika, az do napotkania znaku 'x'.

```c
#include<stdio.h>

int main () {
    char c;
    
    while ((c=getchar())!='x'&&c!='X') {     
    putchar(c);
}
getchar();
return 0;
}
```

***

## Cwiczenie 16 - Napisz program wyswietlajacy tabliczke mnozenia do 13 (uzyj petli !)

```c
#include <stdio.h> 
int main() {
 
int i,j; 
printf("    |");
    for(j=1;j<=13;j++)printf("%4d ",j); 
    printf("\n");
    printf("-----------------");
    for(j=1;j<=13;j++)printf("----");
    printf("\n");
    for(i=1;i<=13;i++)  {
    printf("%4d ",i);
    for(j=1;j<=13;j++)printf("%4d ",i*j); 
    printf("\n");
}
            
getchar();
return 0;
}
```

***

## Cwiczenie 17 - Napisz program liczacy pierwiastki trojmianu kwadratowego: a*x^2+b*x+c=0.

```c
#include <stdio.h> 
#include <math.h>
int main() {
    double a,b,c,delta,x1,x2;
    printf("Podaj a:");
    scanf("%lf",&a);
    printf("Podaj b:");
    scanf("%lf",&b);
    printf("Podaj c:");
    scanf("%lf",&c);
    delta=b*b-4*a*c;
    printf("Delta= %.0lf*%.0lf-%d*%.0lf*%.0lf= %.3lf\n\n",b,b,4,a,c,b*b-4*a*c);
    
   if (delta>0) {
                x1=(-b-sqrt(delta))/(2*a);
                x2=(-b+sqrt(delta))/(2*a);
                printf("x1 = %.2lf \n",x1);
                printf("x2 = %.2lf\n\n", x2);
                printf("Delta wieksza od zero!!!");
               
    
}
    else if (delta==0) {
                x1=x2=(-b)/(2*a);
                printf("x1 = %.0lf \n",x1);
                printf("x2 = %.0lf\n\n", x2);
                printf("Delta rowna sie zero!!");
}
  
   else {
           printf("Blad nie ma rozwiazania");
}

                   
                 
                 
    getchar();
    getchar();
    return 0;
}
```

***

## Cwiczenie 18  - Znajdz liczby o tej wlasnosci, ze suma dzielnikow wlasciwych liczby jest rowna zadanej liczbie, np 6=1+2+3. Sa to tak zwane liczby doskonale. 

```c
#include <stdio.h>
int main() {
    int x,z, suma;
     for (z=2;z<10000;z++) {
     suma=0;
      for (x=1;x<z;x++) {  
         if (z%x==0){
              suma=suma+x;
              }
              }
         if (suma==z) {
              printf("Liczba doskonala=  %d\n\n",suma);
}          
}

getchar();
getchar();
return 0;

}
```
***

## Ćwiczenie 19 - Wyswietl 20 roznych (tj. bez permutacji liczb) trójek pitagorejskich, tzn takich liczb calkowitych dodatnich a,b,c, że a^2 + b^2 = c^2.

```c
#include <stdio.h>
int main() {
    int n;
    int k;
    double zero=0.0;
    double max=-1/zero;
    double min=1/zero;
    double x;
    
    printf("Podaj ilosc liczb conajmniej 2: ");
    scanf("%d",&n);
    
    for (k=1;k<=n;k++) {
        printf("\nPodajliczbe nr %d: ", k);
        scanf("%lf",&x);
                        if (x<min)
                                   min=x;
                                   
                        if (x>max)
                             max=x;
                             }  
                        printf("\nNajwieksza zmiennoprzecinkowa: %.2lf\n\n",max);
                        printf("Najmniejsza zmiennoprzecinkowa: %.2lf",min);
                       
    getchar();                    
    getchar();
    return 0;
}
                        
```
***

## Cwiczenie 20  - Napisz program wypisujacy slownie dzien tygodnia, jezeli nr dnia tygodnia jest znany jako liczba (np.3). Użyj instrukcji switch-case.
