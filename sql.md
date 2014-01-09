``
USE zaklad
GO

CREATE TABLE adres (
  id_adres INTEGER NOT NULL PRIMARY KEY,
  ulica VARCHAR(50) NOT NULL,
  numer VARCHAR(10) NOT NULL,
  kod VARCHAR(20) NOT NULL,
  miejscowosc VARCHAR(20) NOT NULL
);
GO

CREATE TABLE klient (
  id_klient INTEGER NOT NULL PRIMARY KEY,
  id_adres INTEGER NOT NULL REFERENCES adres(id_adres),
  imie VARCHAR(20) NOT NULL,
  nazwisko VARCHAR(20) NOT NULL,
  telefon VARCHAR(20) NOT NULL,
  email VARCHAR(30) NOT NULL,
    data_dodania DATE NOT NULL
);
GO
CREATE TABLE pracownik (
  id_pracownik INTEGER NOT NULL PRIMARY KEY,
  id_adres INTEGER NOT NULL REFERENCES adres(id_adres),
  imie VARCHAR(20) NOT NULL,
  nazwisko VARCHAR(20) NOT NULL
);



CREATE TABLE produkt (
  id_produkt INTEGER NOT NULL PRIMARY KEY,
  nazwa VARCHAR(20) NOT NULL,
  opis VARCHAR(20) NOT NULL,
  cena_netto INTEGER NOT NULL,
  podatek INTEGER NOT NULL,
);
GO
CREATE TABLE zamowienie (
  id_zamowienie INTEGER NOT NULL PRIMARY KEY,
  id_pracownik INTEGER NOT NULL REFERENCES pracownik(id_pracownik),
  id_klient INTEGER NOT NULL REFERENCES klient(id_klient),
  data_zamowienia DATE NOT NULL
);
GO
CREATE TABLE koszyk (
  id_produkt INTEGER NOT NULL REFERENCES produkt(id_produkt),
  id_zamowienie INTEGER NOT NULL REFERENCES zamowienie(id_zamowienie),
  cena_netto INTEGER NOT NULL,
  podatek INTEGER NOT NULL,
  ilosc_sztuk INTEGER NOT NULL DEFAULT 0,
  PRIMARY KEY(id_produkt, id_zamowienie)
);
GO
CREATE TABLE faktura (
  id_faktura INTEGER NOT NULL PRIMARY KEY,
  id_zamowienie INTEGER NOT NULL REFERENCES zamowienie(id_zamowienie),
  id_klient INTEGER NOT NULL REFERENCES klient(id_klient),
  id_pracownik INTEGER NOT NULL REFERENCES pracownik(id_pracownik),
  nr_faktury VARCHAR(20) NOT NULL,
  data_wystawienie DATE NOT NULL,
  data_platnosci DATE NOT NULL,
  czy_oplacona INTEGER NOT NULL DEFAULT 0,
);
GO

## Insert


use zaklad

insert into adres VALUES (1,'Miotka','8','84-223','Linia');
insert into adres VALUES (2,'J.Szutenberga','28','84-200','Wejherowo');
insert into adres VALUES (3,'Zajaca','18','84-222','Kopydłowo');
insert into adres VALUES (4,'Lisa','2','83-200','Zamość');
insert into adres VALUES (5,'Wilka','45','84-440','Zakopane');

insert into klient VALUES (1,5,'Franek','Kłosowski','666-333-444','franek@klosowski.pl','12-12-2013');
insert into klient VALUES (2,4,'Marzena','Guzik','654-234-444','marzena@guzik.pl','12-14-2013');
insert into klient VALUES (3,1,'Danuta','Obłędna','888-542-114','danka@wp.pl','10-16-2013');
insert into klient VALUES (4,2,'Zbyszek','Pyrkowski','897-353-221','focus@gmail.pl','09-25-2013');
insert into klient VALUES (5,1,'Zdzich','Żur','224-111-643','zdzich@gmail.pl','09-30-2013');

insert into produkt VALUES (1,'Viking','Sofa 3F','789','23');
insert into produkt VALUES (2,'Kraków','Fotel 1F','150','23');
insert into produkt VALUES (3,'Target','Sofa 3F+1F','1100','23');
insert into produkt VALUES (4,'Neville','Fotel 1F+1F','650','23');
insert into produkt VALUES (5,'Chesterfield','Sofa 3F','8000','23');
insert into produkt VALUES (6,'Chesterfield','Sofa 3F+1F','10000','23');
insert into produkt VALUES (7,'Diss','Sofa 3F+1F','7000','23');
insert into produkt VALUES (8,'Contra','Fotel 1F','10000','23');

insert into pracownik VALUES (1,2,'Zbigniew','Kolec');
insert into pracownik VALUES (2,2,'Joanna','Kolec');
insert into pracownik VALUES (3,2,'Tomasz','Kolec');
insert into pracownik VALUES (4,2,'Marlena','Kolec');
insert into pracownik VALUES (5,2,'Kajetan','Kolec');

insert into zamowienie VALUES (1,2,3,'12-12-2013');
insert into zamowienie VALUES (2,1,1,'12-15-2013');
insert into zamowienie VALUES (3,4,4,'11-11-2013');
insert into zamowienie VALUES (4,1,2,'12-30-2013');
insert into zamowienie VALUES (5,2,5,'12-24-2013');
insert into zamowienie VALUES (6,3,3,'12-18-2013');

insert into koszyk VALUES (1,2,'150','23','3');
insert into koszyk VALUES (2,1,'750','23','3');
insert into koszyk VALUES (6,3,'10000','23','1');
insert into koszyk VALUES (4,4,'650','23','1');
insert into koszyk VALUES (7,5,'14000','23','2');
insert into koszyk VALUES (8,6,'20000','23','2');
insert into koszyk VALUES (8,2,'10000','23','1');
insert into koszyk VALUES (7,2,'7000','23','1');

insert into faktura values(1,1,3,2,'100/2013','12-12-2013','01-12-2014','1');
insert into faktura values(2,2,1,1,'101/2013','12-15-2013','01-15-2014','1');
insert into faktura values(3,3,4,4,'102/2013','11-11-2013','12-11-2013','0');
insert into faktura values(4,4,2,1,'103/2013','12-30-2013','01-30-2014','0');
insert into faktura values(5,5,5,2,'104/2013','12-24-2013','01-24-2014','1');
insert into faktura values(6,6,3,3,'105/2013','12-18-2013','12-31-2013','0');


## Selecty


use zaklad
go

--1 Wypisuje adresy klientów wraz z ich adresem

SELECT a.kod as kod_pocztowy, a.miejscowosc, w.nazwisko, w.imie 
FROM adres a JOIN klient w ON a.id_adres=w.id_adres;

--2.Wypisuje przypisane faktury do danego pracownika

SELECT n.imie, n.nazwisko,w.nr_faktury
FROM pracownik n JOIN faktura w ON n.id_pracownik=w.id_pracownik ;

--3. Wyswietla ilosc zamowionych produktów koszyku

SELECT n.nazwa, n.cena_netto,  s.ilosc_sztuk AS 'ilość produktów w koszyku'
FROM produkt n JOIN koszyk s ON s.id_produkt=n.id_produkt
ORDER BY s.ilosc_sztuk DESC;

-- 4. Wyświetla ilość zamówionych produktów wraz z datą zamówienia.

SELECT n.nazwa, n.cena_netto,  s.ilosc_sztuk AS 'ilość produktów w koszyku', z.data_zamowienia 
FROM  produkt n  JOIN  koszyk s  ON s.id_produkt=n.id_produkt
			     JOIN zamowienie z on s.id_zamowienie = z.id_zamowienie;


-- 5. Wyświetla informacje o kliencie oraz dane dotyczące zapłaty faktury.

SELECT f.nr_faktury, p.imie +' '+ p.nazwisko as 'klient', f.data_wystawienie ,ABS(DATEDIFF(DAY,  GETDATE(),  f.data_platnosci))AS 'ilosc dni do zaplacenia faktury'  ,f.data_platnosci, pr.nazwa, pr.cena_netto,  ko.ilosc_sztuk AS 'ilość produktów w koszyku', z.data_zamowienia 
FROM  faktura f  JOIN  zamowienie z  ON f.id_zamowienie = z.id_zamowienie
			     JOIN klient k on f.id_klient = k.id_klient
			     JOIN pracownik p on f.id_pracownik = p.id_pracownik
			     JOIN koszyk ko on ko.id_zamowienie = z.id_zamowienie
			     JOIN produkt pr on pr.id_produkt = ko.id_produkt
WHERE f.czy_oplacona = 0 AND DATEDIFF(DAY, GETDATE(),  f.data_platnosci) <= -14

-- 6 Wyświetla dane pracownika który nic nie sprzedał.

SELECT p.id_pracownik,p.imie,p.nazwisko,a.miejscowosc,a.ulica,a.numer 
FROM  pracownik p JOIN adres a ON p.id_adres=a.id_adres
		WHERE p.id_pracownik NOT IN (  SELECT f.id_pracownik FROM faktura f)
		
-- 7.  Wysświetla numer faktury opłaconej oraz kwote do zapłaty netto i brutto 

SELECT count(*) as 'ile pozycji na fakturze', SUM(ko.cena_netto) AS 'Suma Netto', cast(SUM(ko.cena_netto  * (1+cast(ko.podatek as decimal(6,2))/100)) as decimal(8,2))  AS 'Suma Brutto', f.nr_faktury
FROM  faktura f  JOIN  zamowienie z  ON f.id_zamowienie = z.id_zamowienie
			     JOIN klient k ON f.id_klient = k.id_klient
			     JOIN pracownik p ON f.id_pracownik = p.id_pracownik
			     JOIN koszyk ko ON ko.id_zamowienie = z.id_zamowienie
			     JOIN produkt pr ON pr.id_produkt = ko.id_produkt
WHERE f.czy_oplacona = 1
GROUP BY f.nr_faktury		 
ORDER BY f.nr_faktury

-- 8. Wyświetla tylko te faktury które zawierają wiecej niż jedną pozycję.

SELECT count(*) as 'ile pozycji na fakturze', SUM(ko.cena_netto) AS 'Cena Netto', cast(SUM(ko.cena_netto  * (1+cast(ko.podatek as decimal(6,2))/100)) as decimal(8,2))  as 'brutto', f.nr_faktury
FROM  faktura f  JOIN  zamowienie z  ON f.id_zamowienie = z.id_zamowienie
			     JOIN klient k on f.id_klient = k.id_klient
			     JOIN pracownik p on f.id_pracownik = p.id_pracownik
			     JOIN koszyk ko on ko.id_zamowienie = z.id_zamowienie
			     JOIN produkt pr on pr.id_produkt = ko.id_produkt
where f.czy_oplacona = 1
group by f.nr_faktury
having 	count(*) >1
order by f.nr_faktury

 -- 9. Wyświetla średnią sprzedaż danego pracownika.
 
SELECT AVG(ko.cena_netto)AS 'Srednia kwota netto sprzedaży pracownika', SUM(ko.cena_netto)AS 'Suma wszytskich sprzadncyh produktów przez danego pracownika', count(f.nr_faktury) AS 'Ilosć pozycji na fakturze', p.imie + ' ' + p.nazwisko AS 'Dane Pracownika'
FROM  faktura f  JOIN  zamowienie z  ON f.id_zamowienie = z.id_zamowienie
			     JOIN klient k on f.id_klient = k.id_klient
			     JOIN pracownik p on f.id_pracownik = p.id_pracownik
			     JOIN koszyk ko on ko.id_zamowienie = z.id_zamowienie
			     JOIN produkt pr on pr.id_produkt = ko.id_produkt
WHERE f.czy_oplacona = 1
GROUP BY p.imie + ' ' + p.nazwisko
ORDER BY 1

 -- 10. Wyświetla pracownika który nie wystawił żadnej faktury
 
SELECT ( select AVG(ko.cena_netto) from koszyk ko  JOIN  faktura f on ko.id_zamowienie = f.id_zamowienie 
                                                   where f.id_pracownik = p.id_pracownik)AS 'Średnia ze sprzedaży',
        (select SUM(ko.cena_netto) from koszyk ko  JOIN  faktura f on ko.id_zamowienie = f.id_zamowienie 
                                                   where f.id_pracownik = p.id_pracownik) AS 'Suma sprzedaży',                                         
                  (select COUNT(*) from  koszyk ko  JOIN  faktura f on ko.id_zamowienie = f.id_zamowienie 
                                                   where f.id_pracownik = p.id_pracownik) AS 'Ilość wystwionych faktur'                                     
                                                   , p.imie + ' ' + p.nazwisko AS 'Dane Pracownika'
FROM  pracownik p 
			      
	  where p.id_pracownik   not in  (  select f.id_pracownik  from faktura f)  
			    
order by 3

