# WikiMining

## Uvod

Ovaj dokument sadrži kratak opis projekta. Nakon definicije projekta sledi pregled postojećih stavova i shvatanja u literaturi. U daljem tekstu naveden je i softver koji će biti korišćen kao i metode evaluacije.

## Definicija projekta

Tema projekta je sistem [WikiMining](https://github.com/ProfZ/WikiMining/) za predvidjanje popularnosti stranica na Wikipedia-i. Na raspolaganju je broj pregleda po satu i danu, veličina stranice, ostali metapodaci o stanicama kao i same stranice. Zbog obima i broja stranica biće razmatrane samo stranice na engleskom jeziku. 

## Motivacija

Wikipedia, wiki bazirana enciklopedija, postala je jedna od najuspešnijih eksperimenata deljenja znanja na Internetu. Korišćenje "big data" nastalog kao produkt internet zajednice za pristup
informacijama o kolektivnim stanjima svesti u ljudskim društvima postala je nova paradigma u razvoju oblasti računarske društvene nauke. Prirodna primena ovog bi bilo predviđanje
reakcije društva na neki proizvod u smislu popularnosti. Međutim, prevazilaženje velikog jaza između
posmatranja u realnom vremenu i u ranom predviđanju ostaje veliki izazov. U ovom izveštaju
opisujemo problem popularnosti jedne wiki stranice u sledećih nekoliko nedelja na osnovu metapodata svih stranica sa Wikipedia.

## Pregled vladajućih stavova i shvatanja u literaturi

[1] Hanadi Muqbil AL-Mutairi, Muhammad Badruddin Khan (2015) Predicting the Popularity of Trending Articles in the Arabic Wikipedia using Data Mining Techniques 

*Oblast istraživanja*: Formiranje opšteg modela popularnosti Wikipedia stranica na arapskom jeziku.  
*Podaci*: Uzete su u obzir osobine članka iz meta podataka sajta kao i spoljašnji uticaji koji mogu da utiču na popularnost   članka. Primeri spoljnih uticaja koji mogu uticati na popularnost su twitter objave poznatih ličnosti, udarne vesti, posebni aktuelni događaji i slično. Mera popularnosti je broj posetilaca stranice u određenom vremenskom intervalu. Posmatraju se samo clanci na arapskom jeziku.  
*Korišćeni alati*: Korišćene su tehnike data mining-a i text mining-a kao i alat Rapid Miner.  
*Ostvareni rezultati*: Razvijen je model koji omogućava predviđanje popularnosti određenog wikipedia članka na osnovu njegovih osobina i spoljašnjih uticaja.  
*Ograničenja*: Projekat je ograničen na članke koji su na arapskom jeziku.  

[2] [Early Prediction of Movie Box Office Succes Based on Wikipedia Activity Big Data]
(http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0071226#s1)  

*Tema rada*: Predikcija popularnosti filma pre premijere merenjem i analizom nivoa aktivnosti urednika i gledalaca na odnosu filma koji se pretražuje na Wikipedia, poznatoj online enciklopediji.  
*Podaci*: Kako bi se predvidela popularnost filma sledeća 4 parametara su uzeta u obzir: V broj pregleda stranice, U - broj korisnika, tj broj urednika koji su doprineli čanku, E-broj urednika na članku, R - striktnost prilikom uređivanja stranice. Data set koji je korišćen za analizu ovog problema je dostupan na [linku](http://wwm.phy.bme.hu/SupplementaryDataS1.zip).
*Korišćenjeni algoritmi*: Model linearne regresije  
*Ostvareni rezultati*: Postignuto je predikacija popularnosti jednog filma mesec dana unapred.  
Predikcije popularnosti nekog filma je uspešno ostvarena. Upoređivanjem rezultata drugih projekata dobili su dosta preciznu predikciju, jednu od boljih. Autori nisu uspeli da razreše problem predikcije finacijskog uspeha filma što i dalje predstavlja izazov.

## Skup podataka

Za ovu temu je potrebno napraviti skup podataka nad kojim će se vršiti dalje analize. Predviđeno je da se skup formira na osnovu podataka dostupnih na internetu.

**Broj pregleda**

Skup podataka je preuzet sa sajta: [wiki_dumps](https://dumps.wikimedia.org)i sadrži broj pregleda određene stranice i njenu veličinu i datom satu. Format podataka je u formi: jezik ime_stranice broj_pregleda veličina_bitovima i smeštena je u txt datoteku. Na osnovu ovih podataka moguće je izračunati dnevnu, nedelju i mesečnu posećenost stranica. To znači da se moraju skinuti podaci za svaki mesec i dan, i u bazi ažurirati broj pregleda stranice.

**Stranice**

Skup stranica je preuzet sa: [wiki_db](https://en.wikipedia.org/wiki/Wikipedia:Database_download). U dalju analizu ulaze samo one stranice koje imaju posećenost.

## Metod evaluacije

Za analizu podataka koristiće se algoritmi za pronalaženje asocijativna pravila. Asocijativna pravila koristiće se za pronalaženje zavisnosti u podacima i redukovanje dimenzionalnosti. Za odredjivanje popularnosti teme koristiće se podaci o broju pristupa stranicama po vremenu. Za klasifikaciju stranica po temi koristiće se metapodaci koji služe google analytics za pretraživanje stranica. Evaluacija modela vršiće se nad predodredjenim skupom stranica.

## Tehnologije

Za klijentski deo projekta koristiće se sledeće tehnologije:

- AngularJS
- JavaScript
- JQuery
- Ajax
- Bootstrap

Za serverski deo projekta koriste se sledeće tehnologije:

- Java 1.8
- RapidMiner API
- MongoDB

## Plan rada

 - [ ] prikupljanje podataka
 - [ ] transformacija podataka
 - [ ] kreiranje modela
 - [ ] kreiranje softverskog dela
 - [ ] provera modela
 - [ ] kreiranje klijentskog dela
 - [ ] vizuelizacija dobijenih rezultata

## Učesnici u projektu

- Aleksandra Aleksić		  E2 1/2015
- Aleksandar Pejaković 		E2 2/2015
- Aleksandar Birčaković		E2 3/2015
- Miroljub Enjaković	  	E2 75/2015


