# Ročníkový Projekt 2

## Counter-Strike: Global Offensive / Counter-Strike2 

Předmět: Mikropočítačové systémy 

Jméno: Tomáš Doležal 

Třída: T3A 


## 1. Úvod 

V téhle verzi je pokračování minulé, které bylo vpodstatě jen o původu hry CS2


## 2. Síťová komunikace a herní servery

Counter-Strike 2 je online hra, což znamená, že hráči nejsou připojeni přímo mezi sebou, ale komunikují přes herní server.

Server je počítač, který zpracovává informace od všech hráčů a následně je rozesílá ostatním. Díky tomu mají všichni hráči stejné informace o průběhu hry.


## 3. Ping

Důležitým pojmem je ping. Ping udává dobu, za kterou se informace dostane od hráče na server a zpět.

Ping se měří v milisekundách (ms).

Nízký ping znamená rychlejší odezvu hry:

- 0–30 ms = velmi dobré připojení

- 30–60 ms = dobré připojení

- 60–100 ms = hratelné připojení

- nad 100 ms = mohou se objevovat problémy s odezvou
  

## 4. Packet Loss

Dalším důležitým parametrem je packet loss.

Jedná se o ztrátu datových paketů během komunikace mezi hráčem a serverem.

Pokud je packet loss příliš vysoký, může docházet k:

- sekání hry

- teleportování hráčů

- zpožděné registraci zásahů
  

## 5. Sub-Tick systém v CS2

Counter-Strike 2 používá technologii nazývanou Sub-Tick.

Ve starších verzích hry server zpracovával informace pouze v určitých časových intervalech.

Sub-Tick systém umožňuje zaznamenat akce hráče přesněji a server tak dokáže lépe určit okamžik výstřelu nebo pohybu.

- Díky tomu je hra plynulejší a přesnější, zejména na vyšší úrovni hraní.
  

## 6. Význam serverů

Bez serverů by nebylo možné hrát online zápasy ani pořádat profesionální turnaje.

Servery zajišťují férové podmínky pro všechny hráče a umožňují synchronizaci celé hry v reálném čase.


## 7. Praktické měření výkonu hry
Abych lépe pochopil, jak funguje online hraní v Counter-Strike 2, provedl jsem několik jednoduchých měření během hraní.

### Měření FPS

#### FPS (Frames Per Second) udává počet snímků vykreslených za sekundu. Vyšší počet FPS znamená plynulejší obraz.

Během hraní jsem naměřil přibližně:

- průměrné FPS: 205

- nejnižší FPS: 168

- nejvyšší FPS: 278

Měření bylo provedeno pomocí zabudovaného zobrazení výkonu ve hře.

### Měření pingu

#### Ping udává dobu potřebnou k přenosu dat mezi hráčem a herním serverem.

Během několika her/zápasů jsem zaznamenal:

- průměrný ping: 24 ms

- nejnižší ping: 17 ms

- nejvyšší ping: 38 ms

Naměřené hodnoty ukazují, že stabilní a rychlé internetové připojení má významný vliv na kvalitu hraní.

### Packet Loss

Během testování jsem sledoval také packet loss.

Naměřená hodnota byla:

- packet loss: 0 %

Při nízké hodnotě packet lossu nebyly pozorovány žádné problémy s pohybem hráčů ani registrací zásahů.

Při vyšší hodnotě může docházet k zásekům/lagování.

### Vyhodnocení

Z naměřených hodnot vyplývá, že plynulost hry je ovlivněna jak výkonem počítače (FPS), tak kvalitou internetového připojení (ping a packet loss).

Právě kombinace těchto faktorů rozhoduje o tom, jak přesně a plynule hra funguje.


## 8. Herní engine Source 2

#### Counter-Strike 2 využívá moderní herní engine Source 2, který vyvinula společnost Valve.

Oproti původnímu enginu Source přináší řadu technologických vylepšení.

Mezi hlavní změny patří:

- modernější grafické zpracování

- realističtější systém osvětlení a stínů

- kvalitnější fyzika objektů

- vylepšené částicové efekty

- modernizovaná síťová infrastruktura

- efektivnější využití výkonu procesoru a grafické karty


Engine Source 2 využívá pokročilé technologie pro vykreslování obrazu, které umožňují zobrazovat detailnější textury, přesnější odrazy světla a realističtější vizuální efekty.

Díky optimalizovanému zpracování dat dokáže lépe využívat vícejádrové procesory, což přispívá k vyššímu výkonu a stabilnějšímu počtu snímků za sekundu (FPS).

Významnou součástí enginu je také přepracovaný systém fyzikálních výpočtů, který zajišťuje přesnější interakci objektů a efektů ve hře.

Jednou z nejdůležitějších novinek je technologie Sub-Tick.

- Tento systém zaznamenává akce hráčů s vyšší přesností než tradiční tickrate servery, což zlepšuje registraci střelby, pohybu a používání herních předmětů.

- Díky tomu jsou herní situace vyhodnocovány přesněji a výsledky lépe odpovídají skutečným akcím hráčů.

Přechod na engine Source 2 představuje jednu z nejvýznamnějších technologických změn v historii série Counter-Strike a vytváří základ pro další vývoj hry v budoucnosti.


## 9. Hardwarové požadavky hry

#### Pro hraní Counter-Strike 2 je potřeba počítač splňující minimální hardwarové požadavky.

Mezi nejdůležitější součásti patří:

- procesor (CPU)

- operační paměť (RAM)

- grafická karta (GPU)

- úložiště (SSD nebo HDD)

Výkon těchto komponent přímo ovlivňuje počet FPS a celkovou plynulost hry.

Moderní herní počítače často dosahují více než 200 FPS, což hráčům umožňuje rychlejší reakce a přesnější míření.

Proto profesionální hráči používají výkonné počítače a monitory s vysokou obnovovací frekvencí.


## 10.1 Registrace zásahu (Hit Registration)

Ve střílecích hrách (First-Person Shooter) je velmi důležité správné vyhodnocení zásahu protivníka.

Když hráč vystřelí, herní klient odešle informaci o výstřelu na server.

Server následně zpracuje data o poloze hráčů, směru střelby a čase akce a vypočítá, zda došlo k zásahu protivníka.

Pokud server zásah potvrdí, odešle tuto informaci všem hráčům v daném zápase.

Přesnost registrace zásahů je ovlivněna především:

- pingem

- packet lossem

- výkonem serveru

- nastavením síťové komunikace

V Counter-Strike 2 byla registrace zásahů výrazně vylepšena díky technologii Sub-Tick.

Tento systém zaznamenává jednotlivé akce hráčů s vyšší časovou přesností, což umožňuje přesnější vyhodnocení střelby a pohybu.

Díky tomu hra lépe reaguje na skutečné akce hráčů a omezuje situace, kdy hráč vidí zásah, ale server jej nezaregistruje.


## 10.2 Využití procesoru při hraní

Procesor (CPU) patří mezi nejdůležitější součásti počítače při hraní Counter-Strike 2.

Jeho hlavním úkolem je zpracovávat herní logiku a provádět velké množství výpočtů v reálném čase.

Moderní hry dokážou využívat více procesorových jader současně, čímž efektivněji rozdělují výpočetní zátěž.

Procesor během hraní zajišťuje například:

- výpočty pohybu hráčů

- fyziku objektů

- výpočty střelby

- síťovou komunikaci se serverem

- zpracování umělé inteligence botů

Pokud procesor nestíhá zpracovávat všechny potřebné operace, může docházet ke snížení počtu snímků za sekundu (FPS), prodloužení odezvy systému a zhoršení plynulosti hry.

Výkon procesoru je proto velmi důležitý zejména při hraní kompetitivních online her, kde rozhodují i milisekundy.


## 10.3 Grafická karta a vykreslování obrazu

Grafická karta (GPU) zajišťuje vykreslování obrazu zobrazovaného na monitoru.

Je specializována na paralelní zpracování grafických operací a umožňuje plynulé zobrazování herního prostředí.

Při hraní Counter-Strike 2 zpracovává především:

- textury

- osvětlení

- stíny

- částicové efekty

- animace

- vizuální efekty prostředí

Výkonnější grafická karta umožňuje nastavit vyšší grafické detaily a dosahovat vyššího počtu FPS.

Counter-Strike 2 využívá moderní grafické technologie enginu Source 2, které zvyšují kvalitu obrazu a zároveň efektivně využívají výkon současných grafických karet.

Dostatečný výkon GPU přispívá k plynulejšímu hraní a lepšímu vizuálnímu zážitku.


## 10.4 Frekvence obnovování monitoru

Při hraní kompetitivních her je důležitou součástí herní sestavy také monitor.

Frekvence obnovování monitoru udává, kolikrát za sekundu je monitor schopen zobrazit nový obraz.

Nejběžnější hodnoty jsou:

- 60 Hz

- 120 Hz

- 144 Hz

- 240 Hz

- 360 Hz

Vyšší frekvence obnovování umožňuje plynulejší zobrazení pohybu a snižuje vizuální rozmazání rychle se pohybujících objektů.

Díky tomu může hráč rychleji reagovat na herní situace a přesněji sledovat pohyb protivníků.

Z tohoto důvodu profesionální hráči často používají monitory s frekvencí alespoň 240 Hz.


## 10.5 Umělá inteligence ve hrách

V počítačových hrách se využívají různé prvky umělé inteligence (AI).

V Counter-Strike 2 se umělá inteligence používá především pro ovládání botů, kteří nahrazují nebo doplňují lidské hráče.

Boti dokážou:

- pohybovat se po mapě

- nakupovat zbraně a vybavení

- vyhledávat protivníky

- spolupracovat s ostatními členy týmu

- reagovat na herní situace

Jejich chování je založeno na předem definovaných pravidlech a algoritmech, které simulují rozhodování skutečných hráčů.

Přestože nedosahují úrovně zkušených hráčů, představují vhodný nástroj pro trénink a seznámení se s herními mechanikami.


## 10.6 Operační paměť (RAM)

Operační paměť slouží k dočasnému ukládání dat, která procesor aktuálně potřebuje ke své činnosti.

Při hraní Counter-Strike 2 se v paměti RAM ukládají například textury, modely hráčů, zvuky a další herní data.

Pokud má počítač nedostatek operační paměti, musí využívat úložiště, které je výrazně pomalejší.

To může způsobovat prodlevy při načítání dat, pokles výkonu nebo zasekávání hry.

Pro plynulé hraní Counter-Strike 2 se doporučuje alespoň 16 GB operační paměti.


## 10.7 Datová úložiště SSD a HDD

Počítače využívají pro ukládání dat pevné disky HDD nebo modernější SSD.

SSD ukládají data pomocí paměťových čipů a neobsahují žádné pohyblivé části.

Při instalaci Counter-Strike 2 na SSD dochází k rychlejšímu načítání hry, map i dalších herních dat.

Moderní herní počítače proto využívají především SSD disky.


## 10.8 Síťová komunikace mezi klientem a serverem

Counter-Strike 2 funguje na principu komunikace mezi klientem a serverem.

Klient představuje počítač hráče, který odesílá informace o pohybu, střelbě a dalších akcích.

Server tyto informace zpracovává, vyhodnocuje herní situace a rozesílá aktualizovaná data ostatním hráčům.

Kvalita síťového spojení má významný vliv na plynulost a přesnost hraní.

Důležitými parametry jsou zejména ping, packet loss a stabilita internetového připojení.


## 11. Co jsem se při zpracování projektu naučil

Při zpracování tohoto projektu jsem se dozvěděl více o fungování herního enginu Source 2, síťové komunikaci mezi hráčem a serverem a o tom, jaký vliv mají na hraní FPS, ping, packet loss a výkon počítače.

Zjistil jsem také, jak důležitou roli hraje procesor, grafická karta, monitor a internetové připojení při online hraní.

Získal jsem nové informace o registraci zásahů (hitů), fungování technologie Sub-Tick a o využití umělé inteligence ve videohrách.

Projekt mi pomohl lépe porozumět technologiím, které stojí za vývojem moderních počítačových her, nebo minimálně CounterStrike2.

Ještě jsem plánoval, že přidám video, pokud za tohle nedostanu vhodný počet bodů

