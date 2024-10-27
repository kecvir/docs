### Traning
Metodologija: izgradnja temelja kroz rješavanje problema. Polaznicima će biti predstavljen problem koji se može riješiti korištenjem vektorskog prikaza zadanog skupa podataka, s i bez aidb ekstenzije, a zatim će se razmatrati primjena različitih strategija pretraživanja. Poznati primjer je razvoj preporučivačkog sustava gdje korisnici mogu pretraživati koristeći tekst i sliku. Tijekom obuke koristit ćemo ekvivalentan izazov kako bismo ga učinili konkretnim, a ne samo teorijskim.

Iskorištavanje vektora: Otkrivanje ključne uloge i raznovrsnih primjena vektorskih podataka unutar PostgreSQL-a.

Usavršavanje performansi: Procjena performansi aidb i pgvector te usporedba s konkurentskim rješenjima u industriji.
### Srijeda

#### Metodologija: Korištenje AI-a kao PostgreSQL DBA

Umjetna inteligencija (AI) danas je jako popularna. Naći ćete sve vrste informacija o tome kako stvoriti vlastiti AI, koristiti svoje PostgreSQL podatke i još mnogo toga. Međutim, što ako samo želite malo unaprijediti svoje vještine na poslu? Može li AI pomoći onima od nas koji samo pokušavaju snalaziti se?

Kratki odgovor je da. Dulji odgovor je ono što je tema ove sesije. Možete iskoristiti prednosti AI-a za jednostavne zadatke poput generiranja smislenih testnih podataka, jednostavnog optimiziranja upita i još mnogo toga. Dođite i saznajte kako možete upotrijebiti AI u svojim svakodnevnim zadacima, čineći stvari malo jednostavnijima. AI možete koristiti kao alat za bolje učenje PostgreSQL-a i kao način za brže i preciznije izvršavanje određenih zadataka. AI je prisutan i dostupan, stoga ga iskoristite. Pridružite se ovoj sesiji i saznajte kako

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5579/slides/575/AIfortheDBA_pgconfeu.pdf" target="_blank">Slajdovi</a>
#### UNDELETE data FROM table;

PostgreSQL je vrlo dobar u očuvanju sigurnosti vaših podataka. No, nažalost, to vrijedi i obrnuto: nešto što je izbrisano, ostat će izbrisano. U ovom predavanju razmatramo praktične mogućnosti za ponovno vraćanje podataka iz tablica. Ključni elementi su sigurnosne kopije, identifikatori transakcija, pg_dirtyread i umetanja punih stranica. Predavanje vodi održavatelj alata pg_dirtyread.

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5630/slides/562/undelete_from_table.pdf" target="_blank">slajdovi</a>

#### Podešavanje memorije za PostgreSQL u praksi

Ovo predavanje prvo će predstaviti različite načine na koje PostgreSQL može koristiti memoriju, od operativnog sustava, preko širokog klastera pa do po sesiji i po operaciji. Nakon toga, zaronit ćemo u specifičnosti vezane uz različite PostgreSQL parametre kao što su shared_buffers, work_mem, maintenance_work_mem i kako ih postaviti ovisno o vašem opterećenju. Predavanje će također obuhvatiti neka od manje poznatih načina na koje PostgreSQL koristi memoriju, kako možete dijagnosticirati što koristi memoriju u vašem PostgreSQL klasteru i moguće načine da izbjegnete nedostatak memorije. Dodatno, predavanje će obraditi važnost hugepages ne samo za performanse, već i za korištenje memorije na sustavima s velikom memorijom, kao i neka od promjena u postavkama memorije u najnovijim verzijama.

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5935/slides/550/Practical%20Memory%20Tuning%20for%20PostgreSQL%20EU%202024%20SPLIT.pdf" target="_blank">slajdovi</a>

#### Patroni Deployment Patterns - za upravljanje clusterom

Tijekom posljednjih godina, Patroni je postao jedno od najpopularnijih i najuspješnijih rješenja za visoku dostupnost (HA) za PostgreSQL. Rješava probleme razdvojenog mozga i izbora vođe korištenjem RAFT-bazirane distribucijske konsenzus pohrane (DCS) poput etcd-a, koja čuva važne informacije o klasteru. REST API omogućuje praktično upravljanje Postgres čvorovima i njihovom konfiguracijom. Međutim, Patroni je samo predložak za PostgreSQL HA; može se implementirati na širok spektar načina i konfiguracija.

Ova prezentacija će dati kratak pregled Patronija, a zatim raspraviti različite uzorke implementacije (i moguće probleme s njima) s kojima smo se susreli dok smo radili s kupcima na implementaciji PostgreSQL HA. Konkretno, raspraviti će se sljedeće: sinkroni standbys i/ili čitanja replikata, standby klasteri za replikaciju u više regija/zona dostupnosti, mogućnosti i problemi klijentovog prebacivanja te rješenja s problemima DCS-a koji ometaju Patroni.

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5892/slides/544/patroni-deployment-patterns.pdf" target="_blank">slajdovi</a>

#### PostgreSQL dozvole

Korisnici, uloge i dozvole u PostgreSQL-u - zvuči kao dosadna tema, zar ne? Pogrešno. Ova dosadna tema je minirano polje katastrofa koje čeka da se dogodi. Jedna pogrešna GRANT naredba i odjednom vaš praktikant ima DROP privilegije na vašoj produkcijskoj bazi podataka. Oops.

Na ovom predavanju navigirat ćemo opasnim vodama PostgreSQL-ovog sigurnosnog modela. Počet ćemo s osnovama - koja je razlika između korisnika i uloge, zapravo? (Spoiler: ništa, ali ne recite nikome da sam vam to rekao.) Zatim ćemo zaroniti u detalje dozvola, od očitih (SELECT, INSERT) do nejasnih (TRUNCATE, netko?).

Ali čekajte, ima još! Istražit ćemo mračnu umjetnost nasljeđivanja uloga, gdje se dozvole šire poput virusa kroz vašu bazu podataka. Naučit ćete kako stvoriti strukturu dozvola koju svatko može razumjeti. Također ćete naučiti kako provjeriti svoj postav bez da poludite.

Do kraja ovog predavanja imat ćete alate za sigurno postavljanje vaše PostgreSQL instance. Bit će čvrsta kao Fort Knox. Barems, bit će dovoljno čvrsta da vaš CEO ne može slučajno obrisati cijelu tablicu kupaca. Bilo da ste početnik ili iskusni DBA, otići ćete s praktičnim savjetima za smanjenje glavobolje vezane uz sigurnost vaše baze podataka.

### Četvrtak

#### Vodič za nadogradnju vaše PostgreSQL instalacije

Čak ni iskusni PostgreSQL DBA ne može uvijek reći da je nadogradnja između glavnih verzija Postgresa jednostavan zadatak, posebno ako postoje posebni zahtjevi, poput ograničenja vremena nedostupnosti ili ako nešto pođe po zlu. Za manje iskusne DBA-e, bilo što složenije od dump/restore može biti frustrirajuće.

U ovom ću izlaganju opisati zašto nam je potrebna posebna procedura za nadogradnju između glavnih verzija, kako se to može postići i kakvi se problemi mogu pojaviti. Pregledat ću sve moguće načine za nadogradnju vašeg klastera, od klasičnog pg_upgrade do starih metoda poput slony ili modernih metoda poput logičke replikacije. Za sve pristupe dati ću kratak opis kako to funkcionira (ograničen okvirom ovog izlaganja, naravno), primjere kako provesti nadogradnju i nekoliko savjeta o potencijalno problematičnim koracima. Osim toga, dotaknut ću se tema kao što su integracija alata i procedura za nadogradnju s drugim softverom — posrednicima za veze, upraviteljima paketa operativnog sustava, alatima za automatizaciju itd. Ovo izlaganje ne bi bilo potpuno ako ne pokrijem slučajeve kada nešto pođe po zlu i kako se nositi s takvim slučajevima.

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5797/slides/573/pg_upgrades_2023.pdf" target="_blank">slajdovi</a>

#### Pretraživanje nesličnosti: implementacija algoritama pretraživanja vektora u memoriji u PostgreSQL

Pretraživanje vektorskih prostora dobro je proučavana tema u matematici i računalnim znanostima, no prostor problema dobiva novo značenje s porastom AI/ML sustava, posebice generativne AI, koja generira vrlo velike vektore. Prije generativne AI, pretežno smo vidjeli pretraživanje vektora u bazama podataka kroz geospatialne, full-text i bioinformatičke/kemoinformatičke pretrage, koje su sve podržane u PostgreSQL-u, bilo izvorno ili putem ekstenzija. Međutim, svako od ovih područja ima specifične zahtjeve koji su izbjegavali neke od izazova s kojima smo se susreli prilikom pretraživanja vektora iz AI/ML sustava, uključujući korištenje malih (3/4-dimenzionalnih) vektora, korištenje vektora kao filtra umjesto pronalaženja redoslijeda (gdje "K-najbliži susjed" (K=NN) zahtijeva redoslijed) ili dopuštanje pretraživanja s visokom latencijom.

Moderno približno pretraživanje najbližih susjeda (ANN) razvijalo se tijekom posljednjih 25 godina i proizvelo je razne algoritme koji predlažu učinkovite metode pretraživanja preko vektorskih prostora koje mogu vratiti srodne rezultate s visokim stupnjem relevantnosti (mjerenim kao "povratak"). Neki od ovih algoritama uključuju IVF ("inverzijska datoteka"), HNSW ("hierarhijski navigabilni mali svjetovi"), LSH ("hashiranje osjetljivo na lokalnost") i druge. Međutim, većina dizajna ANN algoritama fokusira se na učinkovitost ponašanja indeksa u memoriji – neki od ovih performansnih i relevantnih pretraživačkih koristi možda se neće prenijeti na baze podataka zbog razmatranja poput rasporeda na disku, stalnih ažuriranja, dostupne sistemske memorije i ograničenja resursa zbog drugih radnih opterećenja na istom sustavu.

U ovom izlaganju, detaljno ćemo istražiti razne ANN algoritme koji se mogu implementirati u PostgreSQL i razmotriti što trebamo uzeti u obzir kako bismo osigurali njihovu učinkovitu implementaciju. Istražit ćemo pgvector implementacije IVFFlat i HNSW algoritama te odluke o dizajnu koje omogućuju učinkovito indeksiranje i relevantnost pretraživanja, postizanje višeg stupnja povratka, uključujući strukture podataka indeksa, organizaciju stranica podataka, učinkovito upravljanje ažuriranjima i troškove upita. Također ćemo istražiti PostgreSQL-specifične detalje koji utječu na ove implementacije, uključujući upravljanje zaključavanjem, pozadinske radnike za paralelizam izgradnje indeksa, korištenje izraza za proširenje implementacija indeksa i još mnogo toga. Objasnit ćemo i kompromis između reprezentacija u memoriji i na disku raznih ANN algoritama.

Na kraju ovog izlaganja, razumjet ćete razmatranja koja trebate uzeti u obzir prilikom implementacije ANN algoritma pretraživanja za PostgreSQL, što se također može proširiti na druge sustave baza podataka.

#### Sigurnost PostgreSQL-a: Od Simulacije Napada do Obrane

U današnje digitalno doba, razumijevanje potencijalnih prijetnji vašoj PostgreSQL bazi podataka i načina na koji se protiv njih možete obraniti je ključno. Ova prezentacija, 'Sigurnost PostgreSQL-a: Od Simulacije Napada do Obrane', nudi sveobuhvatno istraživanje ključnih vanjskih prijetnji s kojima se PostgreSQL baze podataka suočavaju.

Počet ćemo s ispitivanjem simulacija stvarnih napada kako bismo istaknuli ranjivost baza podataka na različite sigurnosne prijetnje. Ovi primjeri će pružiti konkretno razumijevanje načina na koji te prijetnje djeluju i rizika koje predstavljaju za vašu PostgreSQL bazu podataka.

Međutim, identificiranje prijetnji je samo pola bitke. Primarni fokus ove prezentacije nije samo otkrivanje prijetnji, već opremanje vas učinkovitom strategijom obrane. Za svaku prijetnju o kojoj ćemo raspraviti, pružit ćemo sažetak zaključaka i preporuka kako biste razumjeli kako najbolje zaštititi svoju PostgreSQL bazu podataka. Ove protumjere su dizajnirane na temelju najboljih praksi i imaju za cilj poboljšanje otpornosti vaše baze podataka na te prijetnje.

Bilo da ste administrator baze podataka, programer ili IT stručnjak zabrinut za sigurnost PostgreSQL-a, ova sesija je osmišljena kako bi vam pružila praktično, primjenjivo znanje za osiguranje vaših baza podataka. Pridružite nam se dok se upuštamo u svijet prijetnji i obrana PostgreSQL-a.

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5554/slides/555/PostgreSQL_Security_PgConf2024_Export.pdf" target="_blank">slajdovi</a>

#### The Wire Protocol 

Trenutni PostgreSQL protokol veze uveden je u verziji 7.3, 2002. godine. Od tada su dodane mnoge nove značajke u pozadinu, no protokol je uglavnom ostao nepromijenjen. Osim PostgreSQL-a, napisane su brojne biblioteke klijenata i posrednici koji koriste taj protokol, pa čak i druge implementacije sustava za upravljanje bazama podataka koje žele biti kompatibilne s PostgreSQL klijentima.

Ovo je obilazak protokola koji počinje od osnova autentifikacije i izvođenja upita do COPY protokola, značajki replikacije i zamišljenog budućeg razvoja.

Teme koje treba obraditi:

Autentifikacija, enkripcija i pregovaranje o značajkama protokola
Upiti, pripremljene izjave i portali
Cjevovodi, upravljanje pogreškama
COPY način
Fizički i logički načini replikacije
Protokol proširenja i verzioniranje

#### Mama, možemo li imati Ggle Maps? – Imamo Ggle Maps kod kuće.

Za one trenutke kada žudite za visokokvalitetnim GIS skupovima podataka, ali je sve previše skupo, OpenStreetMap je besplatno rješenje otvorenih podataka, pokrenuto od strane zajednice.

Trebate li zaista pristup API-jima koji su neizdrživih cijena za ono što želite raditi? Zar već nemamo vodeću kombinaciju baze podataka i GIS backend-a u PostgreSQL-u i PostGIS-u?

Ovaj govor istražuje slučajeve korištenja i što možete učiniti s OpenStreetMap podacima u PostgreSQL-u, kao i koje alate i resurse trebate te kako učitati, ažurirati i pretraživati podatke.

Bit će prikazani primjeri zanimljivih stvari koje "ne-GIS-osoba" može raditi s ovim alatima!

<a href="https://vyruss.org/computing/slides/pgconfeu2024_mom_can_we_have_google_maps.pdf" target="_blank">slajdovi</a>

#### Moderni PostgreSQL za AI aplikacije: s integracijama LLM-a i snažnom pretraživanjem

U ovoj sesiji razgovarat ćemo o proširenju PostgreSQL-a kako bismo podržali moderne AI radne opterećenja. PostgreSQL proširenja su moćan dio Postgres ekosustava. Neka su relativno jednostavna za pokretanje, dok druga donose široke setove nove funkcionalnosti i omogućuju nova radna opterećenja, što omogućava Postgresu da konkurira specijaliziranim bazama podataka. Lantern.dev nudi jedinstven način za postizanje ovoga za AI radna opterećenja, uključujući skalabilno indeksiranje i integracije LLM-a s Postgresom.

Usput, predstavit ćemo i novi način korištenja PostgreSQL proširenja u oblaku. Na temelju našeg iskustva u izgradnji i vođenju Citus-a prvo kao odvojene baze podataka, a kasnije kao PostgreSQL proširenja i usluge u oblaku, razgovarat ćemo o načinima kombiniranja stručnosti specifičnih za radno opterećenje AI aplikacija s operativnim upravljanjem Postgresom.

Ako vas zanimaju AI aplikacije s PostgreSQL-om posebno, ili pokretanje proširenja PostgreSQL specifičnih za radno opterećenje općenito, ova sesija je za vas.

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/6057/slides/570/Ubicloud+Lantern%20PGConf%20EU%202024%20slides.pdf" target="_blank">slajdovi</a>

### Petak

#### Inkrementalni backup

U ovom ću izlaganju raspraviti funkcionalnost inkrementalnog sigurnosnog kopiranja koju sam razvio za PostgreSQL 17. Izlaganje će obuhvatiti način na koji određujemo koje su se podatke promijenile i zašto je odabran taj pristup. Zatim ću detaljno pregledati kako se može napraviti i obnoviti inkrementalno sigurnosno kopiranje te zašto stvari funkcioniraju onako kako funkcioniraju. Ukratko ću se dotaknuti i slučajeva upotrebe ove funkcionalnosti te mogućeg budućeg rada u ovom području.

#### Transarent data encryption

PostgreSQL je najpopularnija open-source baza podataka među programerima. To je jedna od Top 5 baza podataka u svijetu, a potpuno je otvorena i vođena od strane zajednice. No, PostgreSQL, "Car" baza podataka, nema odjeću! U svim praktičnim aspektima, Slonik "hodao je gol" jer ne postoji open-source TDE rješenje koje bi odjevalo slona. Transparentna enkripcija podataka je način na koji se može osigurati zaštita podataka u mirovanju na razini baze podataka, osiguravajući da su podaci šifrirani na disku, kao i u vašim sigurnosnim kopijama, bez potrebe za promjenom aplikacija. Iako TDE nije dostupna u PostgreSQL-u, stvorili smo ekstenziju koja rješava (odijeva slona) ovaj problem i jača sigurnost vaše baze podataka. Pridružite nam se dok pričamo priču o tome kako Slon nema odjeću i kako Percona rješava ovaj problem. Proći ćemo kroz podatke koji pokrivaju razvoj ekstenzije, dodatne sigurnosne prednosti za vašu bazu podataka i ukazati na to što budućnost donosi za TDE.

#### Rješenja i ideje za enkripciju stupaca

Mnogi korisnici traže rješenja za enkripciju podataka iz razloga sigurnosti i usklađenosti. U mnogim slučajevima, ciljana rješenja za enkripciju na razini stupaca mogu biti prikladna i u nekim slučajevima nude čak i bolju sigurnost i usklađenost od enkripcije cijelih diskova ili TDE.

U ovom izlaganju predstavit ću rješenja za enkripciju na razini stupaca, uključujući rješenja s aplikacijske strane i rješenja koja koriste dodatke poput pgcrypto i pgsodium. Također ću obraditi neke kriptografske detalje i tipične sigurnosne i regulatorne zahtjeve za enkripciju u bazama podataka i kako različita rješenja za enkripciju mogu odgovoriti na njih.

Na kraju, možemo razmisliti o tome što bi osnovni PostgreSQL mogao ponuditi za to u budućnosti.

#### Ostalo:
<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5585/slides/561/performance-archaeology-pgconfeu-2024.pdf">Performance Archaeology</a>

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5593/slides/565/PgConfEu2024.pdf">Executing your execution plan</a>

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5792/slides/571/PGConfEU-Borodin-WAL-G.pdf">Hidden gems of WAL-G backup tool</a>

<a href="https://speakerdeck.com/clairegiordano/whats-in-a-postgres-major-release-an-analysis-of-contributions-in-the-v17-timeframe-claire-giordano-pgconf-eu-2024">What's in a Postgres major release? An analysis of contributions in the v17 timeframe</a>

<a href="https://sql.datapage.app/pgconf/2024-sqlpage-badass.pdf">Unearthing the Past with PostgreSQL: How Open Source is Revolutionizing Digital Archaeology</a>

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5569/slides/563/introduction-to-fair-use-tpc-benchmarking-kits.pdf">Introduction to Fair-Use TPC Benchmarking Kits</a>

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5870/slides/572/PostgreSQL%20Observed%E2%80%94%20and%20Explained.pdf">PostgreSQL Observed—and Explained</a>

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5819/slides/574/PGConf.EU%202024-1.pdf">Finding and fixing a data-corruption bug with the help of the community</a>

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5747/slides/559/postgres_statistics_presentation.pdf">A Deep Dive into Postgres Statistics</a>

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5871/slides/556/Postgres%20schema%20migrations%20using%20expand_contract%20-%20PGConf%20EU%202024.pdf">Postgres schema migrations using the expand/contract pattern</a>

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5677/slides/568/pdot.pdf">Exploring Postgres Databases with Graphs</a>

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5846/slides/547/comparing_poolers.pdf">Comparing Connection Poolers for PostgreSQL</a>

<a href="https://anarazel.de/talks/2024-10-23-pgconf-eu-numa-vs-postgresql/numa-vs-postgresql.pdf">NUMA vs PostgreSQL</a>

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/6028/slides/551/security_attacks.pdf">Security attacks on PostgreSQL</a>

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5710/slides/549/csn-snapshots.pdf">High-concurrency distributed snapshots</a>

<a >

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5750/slides/553/my_journey_in_pg_bug_fixing.pdf">My Journey in PostgreSQL bug fixing</a>

<a href="https://www.postgresql.eu/events/pgconfeu2024/sessions/session/5916/slides/578/bmejias_Sparta_Dual_Kings_PG_Active_Active.pdf">Sparta’s Dual Kingship and PostgreSQL Active-Active</a>

