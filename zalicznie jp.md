```c
#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <string.h>
 
int main (void)
{
  char wyraz [100];                        
	int i,z;
	printf ("*******************\n");
	printf ("*Licznik liter  *\n");
	printf ("*******************\n");
	printf ("\n\nTen program liczy litery w wyrazach\n\n");
	printf ("Prosze podaj wyraz \nktory chcesz zanalizowac: ");
	gets (wyraz);         
    int tablica[strlen(wyraz)][2];
    int znalazlem=0;
    int ileZnalazlemLiter=0;
	for (i=0; i < strlen (wyraz); i++)
	{
		if(wyraz[i]>='A' && wyraz[i]<='Z' || (wyraz[i]>='a' && wyraz[i]<='z') ){
		znalazlem=0;
		for(z=0; z < ileZnalazlemLiter; z++){
			if(tablica[z][0] == (int)wyraz[i] || tablica[z][0]+32 == (int)wyraz[i] || tablica[z][0]-32 == (int)wyraz[i] ){
				tablica[z][1] = tablica[z][1]+1;
				znalazlem=1;
				break;
			}
		}
		if(znalazlem==0){
			tablica[ileZnalazlemLiter][0] = wyraz[i];
			tablica[ileZnalazlemLiter][1] = 1;
			ileZnalazlemLiter++;
		}
	}
	}
 		for(z=0; z < ileZnalazlemLiter; z++){
 		
		printf ("\nLiter :%c jest: %d \n",tablica[z][0], tablica[z][1]);
		}
    
 
 
	printf ("\n");
	system ("PAUSE");
	return 0;
}
```
