### Wyklady Niedziela 24-03-2013..

##Obsluga Matlab'a.

***Podstawowe komendy***

* ans - odpowiedz
* foramt compact - wydruk jest bardziej zwarty bez wolnych lini, steruje postacia wydruku
* a=2+2 - przypisanie zmiennej 
* whos  - pokazuje wlasciwosci naszej funkcji
* format short - ustawia wyswietlanie wynik na króki format wydrku
* format long - wynik przedstawiony bedzie w wiekszej precyzji.
* help format - wyswietla pomoc i podstawowe komendy dla format
* realmax - najwieksza liczba reprezentowana dokldanie, to nie jest najwieksza liczba jaka możemy osiagnać.
* inf - informacja o przepelnieniu, wyszlismy poza skale
* realmin - najmniejsza wartosc reprezentowana dokladnie
* eps - epsiolon maszynowy --- najmniejsza liczba ktora dodana do jedynki daje wieksza liczbe od jedynki 1+E>1 (pierwsi sasiedzi kolo jedynki)
* sqrt(_argument_) - obliczanie pierwiastka
* sin(pi) -  sinus pi
* sind(30) - pokazuje w stopniach
* asin() - funkcja odworotna
* [ np 1 2 3 ] - definiowanie vectora, zamiast spacji można sotosować przecinek. Vector wierszowy
* [; ; ;] - vector kolumnowy gdy odzielamy arguenty srednikiem ;
* 1:3 - też wygeneruje vector, sluzy bardziej do ciagów
* ; - gdy odajemy go na koncu obliczen wsytrzymuje wydruk
* plot(x,y) - otwiera okno do rysowania funkcji, okno graficzne
* plot(x,y,'o') - rysowanie za pomoca kólek
* plot(x,y,'o-') - kólka polaczone linia
* plot(x,y,'g-o',x,y1,'r-')  - narysuje dwie funkcje nachodzace sie na siebie kazda w innym kolorze
* >> x=-2*pi:0.1:2*pi;
  >> y=sin(x);
  >> plot(x,y,'o')  ***przykladowa procedura rysowania funkcji
* ezplot('x^2+y^2=4') - narysuje nam kolo o promieniu 4
* clear('zmienna') - usówa zmienna z pamieci
* ' - transpozycja w obliczeniach algebry liniowej
* .* - monożenie wektora i poswstaje wetor. operacje z kropkami licznie element po elemencie. Tak samo można przeprowadzać inne dzialania matemayczne.
   x=[1 2 3 ]
  x =
     1     2     3
  >> y=[4 5 6]
  y =
     4     5     6
  >> x.*y
  ans =
     4    10    18
* factorial(np10)  - oblicza silnie
* primes(np120) - rozklad na lczby pierwsze
* max(x) - najwieksza wartosc w wektorze
* roots() - obliczanie pierwiasków

* . -kropka
* , -przecinek znak oddzielajacy w strukrze, kilka operacji w jednej linijce:
  >> x=2,y=3
  x =
     2
  y =
     3
* ; - srednik umieszczany na koncu lini wstrzymuje wydruk
* : -dwukropek separator w poleceniu tworzenia wektora
* () - nawiasy okragle, zawieraja indeksy elementu macierzy
* [] - nawiasy kwadratowe, tworza tablice liczb lub lancuchów znaków.
* xlabel('funkcja x y') - podisywnie osi x, gdy wstawimy y podpisze y.
* % - oznacza poczatek komentarza
* %{ - zawiera blok linii komentarza
* ... - wielokropek nastepna linia jest kontynuacja natepnej linii
* @ - tworzy uchwyt funkcji np @nazwa
* \ - ukosnik lewy macierzowy operator matematyczny oraz używany do generacji greckich liter i symbolo matematycznych w gafice
* disp - drukuje wyniki
* clc - usówa wszystko z okna Command Window
* clear all - usuówa wszytskie zmienne
* close all - zamyka wszystkie okienka graficzne jeżeli byly pootwierane
* ctr+c - zatrzymuje zadanie gdy sie zapetli
* length(x) - dlugosc elementa wektora
* linespace() - nastepujace polecenie utworzy wektor o n rownoleglych wartosciach np. x=linspace(x0.xk.n)


Możemy sami definiować zmienne

Wszyskie obliczenia sa prowadzone w podwójnej precyzji tybu double.

Program rozróżnia male i Wielkie litery.

## Wyklady po przerwie.

Liczby zapisywane sa w systemie dwójkowym.

znak__mantys_wykladnik

Matysa - skończona liczba liczb

Aby zmienić dokladnosc wyswietlania liczb w MatLab.
File->Preferences->Window Command-> (**short** zminiamy na ***long***)

W Matlabie można przeciazac oberatory.

iloczyn skalarny - x1y1+x2y2+x3y3

W MATLABie nie piszemy programów tylko ***skrypt***.
Matlab jest interpreterem polecen nie potrzebuje kompilatora
Skrypty mozna uruchmiać wpisujac ich nazwe w *Window Command*

Aby zlokalizować pierwistek potrzeba kilka kroków:

f(a)f(b)<0

1. Lokalizacja

2. metoda numeryczna

a) bisekcja

    x1=(b-a)/2 /|f(x)|<E
  
    f(a)f(xi)>0
    
    f(xi)f(b)<0
    
    a=x2
    
b) metoda iteracji prostej
  
    f(x)=0
    
    x=g(x)
    
    xn+1=y(xn)
    
    x2=xp
    
c) regula falsi 
  
    patrzymy w kórym przedziale jest pierwiastek i puszczam sieczna
    
d) Metoda sieczna
  
e) Metoda Newtona-Raphsona - styczna
  
    f(x+h)=f(x)+1/1!hf'(x)+1/2!hf''(x)...
    
    f(x+x1-x)=f(x)+hf'(x)=0
    
    0=f(x+x1-x)=f(x)+hf'(x) --> x2=x-(f(x)/f'(x))
    
    
  
## Petla w Matlab'ie
  
  Petla FOR: 
  
    for s=0.0:0.01:1.0
        disp(s)
    end

  Warunek IF:
  
    r=5
    c=5
    
    if r == c
      disp('sylwek');
      else
         disp('zonk');
      end


# Zajecia 14.04.2013 mala powtórka

### Zmienne zapisywane w systemie podwójnej precyzji:

* realmax
* realmin
* eps 1+eps>1

Skalarne a=1

Wektory 
        x=[1 2 3]
        y=[1;2;3]
Macierze 
        [1,2;2,3]

Polecenia:

        who wyswietla informcje o zmiennych
        whos
        clear all - czsci tabele
        
### Obliczenia numeryczne(symboliczne)

      okna:
        komendy
        grafika
        edytor dzielimy na skrypt i funkcje

Skrypty:
        Możemy tworzyć petle for, if, while
        Obliczać sumowania

Operacje:
      Algebra liniowa
        dodawnia +
        odejmowania -
        mnożenia *
      Tablicowe(kropkowe)
        element * element
        
Te operacje można realizować przez petle.

# Cwiczenia

### Cwiczenie 2 Operacje na liczbach 0blicz:

      x=(-log(2.4)+sqrt(sin(4)-4*exp(3.4)))/(2*pi)

      x=sqrt(4*exp(12.4))/(2*tan(pi*0.47))
      
***
### Sprawdzanie numeryczne tożsamosci trygonoetrycznej dla kilku wartosci katów alfa i beta np. pi/2, 0.366pi itp

       w=[]
    for b=0:0.1:1
       disp(b);

      c= cos(b).^2+sin(b).^2-1;
      w=[w,c]
    end
    w
***
### Zadanie z cos(alfa)+cos(beta)

    alfa=pi/2
    beta=0.366*pi
    z=(cos(alfa)+cos(beta))-(2*cos(0.5*(alfa+beta)))*(cos(0.5*(alfa-beta)))
    
***

### Generowanie wektorów, przetestuj wyrżenia:

    a=[1 2 3];
    b=[1,2,3];
    c=[1;2;3];
    y=b'
    c==y
    c(1)=5
    b(2)=6
    clc
    
### Przykład b)
    
    c==y
    d=[-1.3*sin(sqrt(5))*(log(6)-5)]
    e=[1:10]
    e=[1:.1:10]

***
### Zadanie - Dostep do elementów

### Przyklad a)

    a=[1:5]
    a(1),a(2)
    a(10)
    a(10)=123%co się stanie, przecież a ma rozmiar 5 
    Program pokaż blad bo tablica jest za mala, trzeba zamiast a=[1:5] wpisać a=[1:10]
    
### Przyklad b)

    b=[2:2:20]
    b/2
    2\b
    c=[1:10]
    b/c
    b./c
    
### Zadanie - Interpolacja
    
    x=[1,2,3]
    y=[3.20,3.29,3.32]
        
    p=polyfit(x,y,2)
    x1=1:0.1:3;
    y1=polyval(p,x1)
    plot(x,y,'o',x1,y1,'--')
    
### Aproksymacja 

    x=[1,2,3]
    y=[3.20,3.29,3.32]
        
    p=polyfit(x,y,2)
    p1=polyfit(x,y,1)
    x1=1:0.1:3;
    y1=polyval(p,x1)
    y2=polyval(p1,x1)
    plot(x,y,'o',x1,y1,'--',x1,y2)


## Macierze

      A=[1 2 3;4 5 6;7 8 9]
      B=A'
      A(2,3)
      C=[1:10;11:20;21:30;31:40]
      C(1:2,1:4)
      C(2:3,1:1)
      C(1:1,5:8)
      D=[C,[1;2;3;4]]
      Z=zeros(2,4)
      
      
      x=rand(4,4)
      F=5*ones(3,3)
      F=F*2
      F=F/5
      G=4*ones(3,3)
      G/F
      G./F
      G*F
      G.*F
      
### Operacje macierzowe

    z=rand(4,4)
    det(z)
    sum(z)
    min(z)
    max(z)
    x=inv(z)
    x*z
    diag(z)
    rank(z)
    
### Uklad równan liniowych

    a=[1 -4 3 5;3 1 -2 7;2 1 1 8;-1 -2 -5 -2];
    b=[-7;14;5;4];
    [x]=[a]\[b]
  
### Liczby zespolone

    a=4+3i
    b=5+2i
    a+b;a-b;a*b;a/b;
    real(a)
    imag(b)
    conj(a)
    abs(a)
    angle(a)
    c=5*(cos(0.6435)+i*sin(0.6435))
    d=5*exp(i*0.6435)
    
#Wykresy

### Dwuwymiarowy wykres

    x=-10:.005:40;
    y=[1.5*cos(x)+4*exp(-.01*x).*cos(x)+exp(.07*x).*sin(3*x)];
    plot(x,y)
    
### Wykres3D

    [x,y]=meshgrid(-3:.12:3);
    z=sin(x).*exp(y)+x.*y;
    mesh(x,y,z);
    
#Funkje

### Otwieranie funkcji z zapisanej w skrypcie w WindowCommand

    function[val]=kwadratowa(a,b,c,x)
    
    val=a*x.^2+b*x+c;
    end
    
Funkcje wywolujemy poleceniem>> kwadratowa(1,1,1[1 2 3])





    

    

