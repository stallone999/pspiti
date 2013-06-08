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

void wyswietl(struct student Studenci[MAX_STUDENTOW], int iloscStudentow){
     int k;
     for (k=0;k<iloscStudentow;k++)
        printf("%s %s %d\n", Studenci[k].imie,Studenci[k].nazwisko, Studenci[k].ocena);
        }
    
int main() {
    int k,iloscStudentow=0;
    struct student Kowalski={"Jan", "Kowalski", db};
    struct student Studenci[MAX_STUDENTOW];
    FILE *plik;
    const char * const nazwaPliku="studenci.txt";


    Studenci[0]=Kowalski;
    iloscStudentow++;
    
    strncpy(Studenci[1].imie, "Adam",12);
    Studenci[1].imie[11]='\0';
    strncpy(Studenci[1].nazwisko,"Wisniewski",16);
    Studenci[1].nazwisko[15]='\0';
    Studenci[1].ocena=dst;
    iloscStudentow++;
    
    //Studenci[1].ocena=444;
    
    if((plik=fopen(nazwaPliku,"w"))==NULL){
                                           fprintf(stderr,"Nie moge otowrzyc pliku %s\n", nazwaPliku);
                                           exit(2);}
                                           
    for (k=0;k<iloscStudentow;k++)
        fprintf(plik,"%s %s %d\n", Studenci[k].imie,
        Studenci[k].nazwisko, Studenci[k].ocena);
    
    
    if(fclose(plik)!=0) {
                        fprintf(stderr,"Nie moge znalezc pliku %s\n",nazwaPliku);
                        exit(3);}
                        
    wyswietl (Studenci,iloscStudentow);  
       
    getchar();
    return 0;
}

```

## Zadanie z dodawaniem nowego studenta.

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

void wyswietl(struct student Studenci[MAX_STUDENTOW], int iloscStudentow){
     int k;
     for (k=0;k<iloscStudentow;k++)
        printf("%s %s %d\n", Studenci[k].imie,Studenci[k].nazwisko, Studenci[k].ocena);
        }
void zapisz(struct student Studenci[MAX_STUDENTOW], int iloscStudentow) {
     int k;
     FILE *plik;
     const char * const nazwaPliku="studenci2.txt";
     
      if((plik=fopen(nazwaPliku,"w"))==NULL){
                                           fprintf(stderr,"Nie moge otowrzyc pliku %s\n", nazwaPliku);
                                           exit(2);}
     for (k=0;k<iloscStudentow;k++)
        fprintf(plik,"%s %s %d\n", Studenci[k].imie,
        Studenci[k].nazwisko, Studenci[k].ocena);
        
        
     if(fclose(plik)!=0) {
                        fprintf(stderr,"Nie moge znalezc pliku %s\n",nazwaPliku);
                        exit(3);}
}

int dodajStudenta(struct student Studenci[MAX_STUDENTOW], int iloscStudentow, struct student nowyStudent) {
     Studenci[iloscStudentow]=nowyStudent;
     iloscStudentow++;
     return iloscStudentow;
     }
     

int main() {
    int k,iloscStudentow=0;
    struct student Kowalski={"Jan", "Kowalski", db};
    struct student Studenci[MAX_STUDENTOW];
    
    struct student nowyStudent;
    printf("Podaj imie nowego studenta\n");
    scanf("%s",nowyStudent.imie);
    nowyStudent.imie[11]='\0';
    
    printf("Podaj nazwisko nowego studenta\n");
    scanf("%s",nowyStudent.nazwisko);
    nowyStudent.nazwisko[15]='\0';
    
    printf("Podaj ocene nowego studenta\n");
    scanf("%d",& nowyStudent.ocena);
    
    
        


    Studenci[0]=Kowalski;
    iloscStudentow++;
    
    strncpy(Studenci[1].imie, "Adam",12);
    Studenci[1].imie[11]='\0';
    strncpy(Studenci[1].nazwisko,"Wisniewski",16);
    Studenci[1].nazwisko[15]='\0';
    Studenci[1].ocena=dst;
    iloscStudentow++;
    
    //Studenci[1].ocena=444;
    
    
    iloscStudentow=dodajStudenta(Studenci,iloscStudentow, nowyStudent);            
    zapisz (Studenci,iloscStudentow);
    wyswietl (Studenci,iloscStudentow);  
  
    printf("\n%d",iloscStudentow);
    getchar();
    getchar();
    return 0;
}
```
