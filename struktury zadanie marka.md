```c
#include <stdio.h>
#include <string.h>
#include<stdlib.h>

#define MAX_STUDENTOW 15

enum oceny {ndst=2, dst, db, bdb };

struct student {
      char imie[12];
      char nazwisko[16];
      enum oceny ocena;
};
/********************************************************/
void wyswietl(struct student Studenci[MAX_STUDENTOW],int iloscStudentow){
int k;
for (k=0;k<iloscStudentow;k++)
       printf("%s \t%s\t %d\n", Studenci[k].imie,
       Studenci[k].nazwisko, Studenci[k].ocena);
getchar();
}
/********************************************************/
void zapisz(struct student Studenci[MAX_STUDENTOW],int iloscStudentow){
int k;
FILE *plik;
const char * const nazwaPliku="studenci.dat";
if((plik=fopen(nazwaPliku,"w"))==NULL){
                                          fprintf(stderr,"Nie moge otowrzyc pliku %s\n", nazwaPliku);
exit(2);}
for (k=0;k<iloscStudentow;k++)
       fprintf(plik,"%s %s %d\n", Studenci[k].imie,
       Studenci[k].nazwisko, Studenci[k].ocena);

   if(fclose(plik)!=0) {
                       fprintf(stderr,"Nie moge znalezc pliku %s\n",nazwaPliku);
   exit(3);
}

}
/****************************************************/
int dodajStudenta(struct student Studenci[MAX_STUDENTOW],
int iloscStudentow,struct student nowyStudent){
Studenci[iloscStudentow]=nowyStudent;
iloscStudentow++;
return iloscStudentow;
}
/**************************************************/
struct student generujStudenta(void){
struct student y;
printf("Podaj imie nowego studenta\n");
   scanf("%s",y.imie);
y.imie[11]='\0';
printf("Podaj nazwisko nowego studenta\n");
   scanf("%s",y.nazwisko);
y.nazwisko[15]='\0';
printf("Podaj ocene nowego studenta\n");
   scanf("%d",&y.ocena);

return y;
}

/*****************************************
int dodaj(struct student Studenci[],int iloscStudentow){
int n=0;
FILE *plik;
const char * const nazwaPliku="studenci.dat";
while(fscanf(plik,"%s %s %d",Studenci[n].imie,Studenci[n].nazwisko,Studenci[n].ocena)==3)n++;
return n;
}
***********************************************************/
int  czytaj(struct student y[],int iloscStudentow){
int n=0;
const char * const nazwaPliku="studenci.dat";
FILE *plik;
plik=fopen(nazwaPliku,"r");
if((plik=fopen(nazwaPliku,"r"))==NULL){fprintf(stderr,"Nie moge otowrzyc pliku %s\n", nazwaPliku);
exit(2);}
while(fscanf(plik,"%s %s %d",y[n].imie,y[n].nazwisko,&y[n].ocena)==3)n++;
if(fclose(plik)!=0) {
                       fprintf(stderr,"Nie moge znalezc pliku %s\n",nazwaPliku);
   exit(3);
}
return n;
}
/*******************************/
int main() {
   int k,iloscStudentow=0;
   struct student Kowalski={"Jan", "Kowalski", db};
   struct student Studenci[MAX_STUDENTOW];
   struct student nowyStudent,y;
const char * const nazwaPliku="studenci.dat";


   Studenci[0]=Kowalski;
   iloscStudentow++;

   strncpy(Studenci[1].imie, "Adam",12);
   Studenci[1].imie[11]='\0';
   strncpy(Studenci[1].nazwisko,"Wisniewski",16);
   Studenci[1].nazwisko[15]='\0';
   Studenci[1].ocena=dst;
   iloscStudentow++;
   iloscStudentow=dodajStudenta(Studenci,iloscStudentow,nowyStudent);
   wyswietl(Studenci,iloscStudentow);
   //Studenci[1].ocena=444;
   nowyStudent=generujStudenta();
   zapisz(Studenci,iloscStudentow);
   
   czytaj(Studenci,iloscStudentow);
   wyswietl(Studenci,iloscStudentow);
   return 0;

}
```
