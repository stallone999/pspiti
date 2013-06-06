```c
#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <string.h>
#include <math.h>
int main (void)
{
  double szerokosc=0;
	char polkula='N';
	double strona=1;
	printf("Witam w programie, ktory oblicza dlugosc dnia \nna podstwie szerokosci gograficznej! \n\n");
	printf("Podaj litere-S lub N w zaleznosci od tego na jakiej polkuli sie znajdujesz: \n");
	scanf("%[SN]s", &polkula);
	printf("\nPodaj szerokosc dla ktorej chcesz obliczyc dlugosc dnia np:'33.44': \n");
   	scanf("%lf", &szerokosc);
    if(polkula=='S'){
    	strona=-1;	
    }
    double deklinacjaSlonca=23.5;
    double szerokoscRadiany = strona*szerokosc*M_PI/180;
    double deklinacjaSloncaRadiany = deklinacjaSlonca*M_PI/180;
    double czasRadiany =acos(-1 * tan(szerokoscRadiany)*tan(deklinacjaSloncaRadiany));
    double czasStopnie = (czasRadiany*180/M_PI)*2;
    int czasGodziny =(int) czasStopnie/15;
    int czasMinuty = ((czasStopnie/15) - czasGodziny)*60;
	printf ("\nCzas w stopniach wynosi  %lf.\n",czasStopnie);
	printf ("\nDla danej szerokosci geograficznej dzien bedzie trwal %d godzin i %d minut.\n",czasGodziny,czasMinuty);
	getchar();
	getchar();
	return 0;
}

```
