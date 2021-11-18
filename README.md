# JavaDesetaVjezba

10.Deseta laboratorijska vježba
10.1. TEMA VJEŽBE
Svrha laboratorijske vježbe je implementacija funkcionalnosti koje će
se izvršavati paralelno s ostalim aktivnostima, a temeljit će se na
višenitnosti i sinkronizaciji niti.
10.2. ZADATAK ZA PRIPREMU
Proširiti rješenje devete laboratorijske vježbe na način da se kopira
rješenje te preimenuje u naziv koji sadrži indeks „10“, umjesto „9“. Osim
same mape s projektom, potrebno je promijeniti i naziv projekta unutar
IntelliJ-a korištenjem opcije „Refactor->Rename“. Program je potrebno
proširiti na način opisan u nastavku:
1. Kreirati paket „hr.java.covidportal.niti“.
2. U paketu iz prvog koraka kreirati klasu „NajviseZarazenihNit“ koja
implementira sučelje „Runnable“ i implementira logiku s kojom se
određuje naziv županije koja ima najveći postotak zaraženih
stanovnika korištenjem lambda izraza.
3. Nit iz drugog koraka je potrebno pokrenuti kod prikazivanja ekrana
za pretragu županija i u konzolu svakih 10 sekundi ispisivati naziv
županije koja ima najveći postotak zaraženih stanovnika.
4. Istu funkcionalnost definirati na način kako bi se ispisivala umjesto
naslova ekrana korištenjem klase „TimeLine“ opisane na sljedećoj
poveznici: https://stackoverflow.com/questions/36577687/usetimeline-to-trigger-a-void-method-every-certain-seconds-javafx.
5. Metodu koja služi za kreiranje konekcije s bazom podataka potrebno
je proširiti ključnom riječju „synchronized“ i proglasiti kritičnim
isječkom. Također je potrebno na razini klase koja sadrži metode za
komunikaciju s bazom kreirati varijablu s nazivom
„aktivnaVezaSBazomPodataka“ tipa „Boolean“ koja će označavati kad
je neka od operacija s bazom podataka u tijeku (slično kao i varijabla 
„isRezervacijaUTijeku“ iz primjera sinkronizacije niti koji je objašnjen
na predavanjima).
Svaku operaciju s bazom podataka prebaciti u nit koja se pokreće kad
se pritisne gumb za izvršavanje operacije bazom podataka i dodijeliti
joj proizvoljno ime. Za svaku nit kreirati odgovarajuću klasu unutar
paketa iz prvog koraka.
Korištenjem metoda „wait“ i „notifyAll“ implementirati sinkronizaciju
koja će omogućavati da je u svakom trenutku samo jedna operacija s
bazom podataka aktivna, slično kao što je to implementirano na
primjeru kino-dvorane s predavanja.
Primjer izvođenja programa je prikazan na sljedećem videu:
https://youtu.be/WRUW1c7W7xY.
