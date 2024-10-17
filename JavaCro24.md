# JavaCro 24
###  dan 1:
*  Otkrijte kako smo implementirali praćenje korisničkih aktivnosti na našem projektu. Pratimo sve promjene u bazi podataka kako bismo osigurali integritet i transparentnost podataka, bilježeći svaku operaciju umetanja (insert), ažuriranja (update) i brisanja (delete). Dodatno, nadziremo korisničke akcije koristeći Elasticsearch, prateći zahtjeve i odgovore kako bismo razumjeli interakcije korisnika i pretrage podataka. Saznajte više o našim početnim konceptima, izazovima i evoluciji rješenja, te dobijte praktične uvide za robusni nadzor u Java aplikacijama.
*  Zaronit ćemo u zagonetni svijet umjetne inteligencije kako bismo razjasnili mitove i zablude koje često zamagljuju njezino razumijevanje. Istražit ćemo kako funkcioniraju veliki jezični modeli (LLM-ovi) poput GPT-a, koristeći ogromne količine podataka i sofisticirane algoritme za generiranje teksta sličnog ljudskom. Također ćemo raspravljati o široj kategoriji generativne umjetne inteligencije, koja uključuje tehnologije sposobne za stvaranje sadržaja, od teksta do slika i glazbe, čime ćemo ilustrirati mogućnosti i potencijal tih sustava. Kako bismo dodatno prikazali svestranost umjetne inteligencije, istražit ćemo arhitekturu pod nazivom Retriever-Augmented Generation (RAG), koja kombinira snage pretraživanja informacija s generativnim modelima kako bi poboljšala točnost i relevantnost odgovora. Primjeri korištenja RAG-a uključuju poboljšanje odgovora tražilica i unaprjeđenje interaktivnih edukacijskih alata, pokazujući njegove praktične primjene u raznim industrijama. Ova sveobuhvatna analiza pružit će čvrste temelje za razumijevanje trenutačnog stanja i budućeg potencijala AI tehnologija.
*  Otključavanje AI sposobnosti u Javi: Istraživanje najnovijih alata

Nedavni porast razvoja umjetne inteligencije dramatično je transformirao razvojni ekosustav više nego bilo koji drugi trend u posljednjih nekoliko godina. Mnogi programeri sada svakodnevno koriste AI alate poput ChatGPT-a i Copilota ili stvaraju aplikacije koje integriraju razne AI API-je kako bi uključili funkcionalnosti umjetne inteligencije.

U početku je Python bio dominantan jezik za razvoj AI-ja zbog svoje snažne prisutnosti u AI zajednici još prije nego što je došlo do velikog interesa. Međutim, s rastom popularnih AI API-ja, i drugi programski jezici počeli su implementirati AI mogućnosti. Posebno se Java istaknula kao značajan igrač u ovom području.

U ovom predavanju istražit ćemo što Java, a posebno Spring framework, nudi za razvoj umjetne inteligencije. Pregledat ćemo biblioteke kao što su Spring AI i LangChain4J te prikazati kako ih se može koristiti za integraciju AI funkcionalnosti u Java aplikacije.  
*  Napredne Kotlin Tehnike za Spring Programere

Kao iskusni programer, vjerojatno ste već upoznati sa Springom. No, Kotlin može podići vaše iskustvo razvoja sa Springom na višu razinu!
Pridružite se ovom webinaru i naučite kako:
- Dodati novu funkcionalnost postojećim klasama koristeći Kotlin ekstenzijske funkcije.
- Koristiti Kotlin DSL za definiranje bean-ova.
- Bolje konfigurirati svoju aplikaciju koristeći `lateinit`.
- Koristiti sekvence i zadane vrijednosti argumenata kako biste pisali izražajniji kod.
Na kraju ovog predavanja, imat ćete dublje razumijevanje naprednih Kotlin tehnika koje su vam dostupne kao Spring programeru i moći ćete ih učinkovito primijeniti u svojim projektima.
* Praktični uvod u OpenTelemetry praćenje

Praćenje tijeka zahtjeva kroz različite komponente u distribuiranim sustavima je ključno. S porastom mikroservisa, njihova važnost postala je od kritične važnosti. Već su se koristili neki vlasnički alati za praćenje: Jaeger i Zipkin prirodno padaju na pamet.

Observabilnost se temelji na tri stupa: zapisnicima (logovi), metrikama i praćenju (tracing). OpenTelemetry je zajednički napor da se uvede otvoreni standard za te stupove. Jaeger i Zipkin su se pridružili ovom naporu i sada su kompatibilni s OpenTelemetryjem.

U ovom izlaganju opisat ću gore navedeno u više detalja i prikazati (jednostavan) slučaj upotrebe kako bih demonstrirao kako možete imati koristi od OpenTelemetryja u svojoj distribuiranoj arhitekturi

### dan 2:
*  Mutanti u akciji: Koliko su učinkoviti vaši unit testovi?

Pišemo testove kako bismo riješili bugove, provjerili funkcionalnost i olakšali održavanje. Koristeći pokrivenost koda kao mjerilo, mogli bismo smatrati da smo sigurni i da su naši testovi besprijekorni. Ali kako možemo biti sigurni da su naši testovi u redu? Činjenica da testovi pokrivaju kod ne znači da kod ispravno radi. Nedostatak asercije može otvoriti vrata za brojne bugove!

U ovom predavanju zakoračit ćemo u svijet testiranja mutacija. Generiranjem mutanata, tj. neispravnih verzija vašeg koda, mjerimo koliko su testovi učinkoviti u otkrivanju bugova. Pokrit ćemo alate za mutacijsko testiranje, kako funkcioniraju, kako početi i kako ih integrirati u vaše build procese.
*  Učenje uz pomoć umjetne inteligencije u razvoju softvera i obrazovanju iz programiranja

S brzim napretkom umjetne inteligencije, posebno velikih jezičnih modela (LLM-ova), područje razvoja softvera drastično se promijenilo u posljednjih nekoliko godina. AI alati i usluge specijalizirani za razvoj softvera, poput GitHub Copilot-a, Amazon CodeWhisperer-a, Tabnine-a i drugih, kao i općenitiji alati poput ChatGPT-a, ne samo da omogućuju generiranje i dovršavanje koda, već se ističu i u složenijim zadacima kao što su razumijevanje koda, generiranje testnih slučajeva, reverzno inženjerstvo i refaktoriranje koda. Integrirani u razvojna okruženja (IDE), oni podržavaju produktivnost programera i pojednostavljuju procese razvoja softvera. Ova prezentacija istražuje transformativnu ulogu AI asistenata u programiranju u obrazovanju za razvoj softvera, posebno u programiranju na preddiplomskim kolegijima na našim sveučilištima i visokim školama. Njihova integracija u visoko obrazovanje, posebno u online učenje s manje iskusnim studentima, donosi mnoge prilike, ali i izazove. Želimo predstaviti naša otkrića i pružiti uvide u to kako se ti AI alati mogu iskoristiti za obogaćivanje obrazovnih praksi i poboljšanje ishoda učenja na kolegijima iz razvoja softvera, istovremeno adresirajući brige povezane s akademskim integritetom i plagijatom te održavajući visoke akademske standarde u evoluirajućem području obrazovanja iz softvera.
*  Demistificiranje Java Virtual Threads - naučene lekcije iz njihove primjene u GlassFish "keynoteu"

Želite li razumjeti kako Java Virtual Threads zapravo funkcioniraju i jesu li mitovi koje ste čuli o njima istiniti ili ne? Pridružite mi se da to saznate.

U ovoj ćemo sesiji istražiti kako Java Virtual Threads rade, razbiti mitove i ponuditi praktične smjernice o njihovom učinkovitom korištenju. Na temelju mog iskustva s GlassFish i Grizzly, razgovarat ćemo o tome kada i kako koristiti virtualne niti za optimizaciju performansi i korištenja resursa u vašim aplikacijama. Uz to, istaknut ćemo uobičajene zamke koje treba izbjegavati.

Razotkrit ćemo nekoliko mitova o virtualnim nitima i objasniti zašto se ne biste trebali bojati koristiti ih. Osim toga, pozabavit ćemo se pitanjem predstavljaju li virtualne niti konkurenciju reaktivnom programiranju u Javi ili mogu li se dobro uklopiti zajedno.

Pridružite mi se dok otkrivamo misterije Java Virtual Threads i otvaramo put ka učinkovitijem, responzivnijem Java ekosustavu.

*  Java Putovanje: Slavimo Baštinu, Prihvaćamo Budućnost – HUJAK #Java Zajednički Ključni Govor**

Zaronite u živopisni svijet Jave kroz zajednički ključni govor HUJAK-a (Hrvatska Java Korisnička Udruga). Otkrit ćemo trenutno stanje robusnog tehnološkog ekosustava Jave, prikazujući njezin napredak i značajke uvedene u nedavnim ažuriranjima, te raznolike okvire i alate koji potvrđuju status Jave kao vodeće platforme za razvoj softvera već više od 29 godina. Ističući razvojne projekte poput JDK-ovih projekata Amber, Valhalla, Loom, Graal, Panama i drugih, istražit ćemo ključne značajke jezika i transformacijska poboljšanja Jave koja su dostupna u verzijama s dugoročnom podrškom (LTS) poput Jave 17 i Jave 21, kao i nove dodatke u ovogodišnjim Javi 22 i 23. Raspravljat ćemo o Virtualnim Nitima, Strukturalnoj Konkurentnosti, Foreign Function & Memory API, Vector API, GCs, Implicitnim Deklaracijama, String Šablonama, Scoped Vrijednostima i mnogim drugim temama. Osim tehničkih napredaka, rasprava će obuhvatiti i njihove implikacije na cjeloživotno učenje i karijerne prilike u tehnološkoj industriji. Zajedno ćemo proslaviti trajni utjecaj Jave kroz njezinu baštinu i budućnost te zamisliti njezinu ulogu u modernom razvoju softvera.
