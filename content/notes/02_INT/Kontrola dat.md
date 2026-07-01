---
date: 2025-10-21T22:43:00
author: n7x3n
---
- proces ověřování, zda jsou data správně a bez chyb. To znamená jestli jsou konzistentní. 
- Data mohou být poškozena (rušením, chybou při zápisu, překlepem).
- Je potřeba ověřit jejich integritu – zda se nezměnila.
- Někdy stačí chybu odhalit (detekce), jindy je nutné ji i opravit.
## Chyby v datech
Při přenosu je narušení nebo změna dat během jejich přenosu mezi zařízeními, způsobená například rušením nebo ztrátou paketů
### Přenosové chyby
- Vznikají při přenosu dat (např. po síti, Wi-Fi, Bluetooth). 
- Příčiny: rušení, šum, slabý signál, fyzické poškození média (škrábanec na CD). 
- Typické projevy: změněný bit (1 místo 0), „rozbitý“ obrázek, nečitelný soubor.
### Lidské chyby
- Vznikají při ruční práci s daty. 
- Příčiny: překlep, chybějící znak, přeházené číslice. 
- Typické příklady: špatně opsané rodné číslo, chybný variabilní symbol u platby.
### Chyby při ukládání dat
- Vznikají při zápisu nebo čtení z paměti/uložiště. 
- Příčiny: vadný sektor na disku, opotřebovaná flash paměť. 
- Projevy: soubor nejde otevřít, hláška „CRC error“.
### Úmyslné chyby (manipulace s daty)
- Záměrná změna nebo podvržení dat. 
- Příklady: 
	- Úprava obrázku / dokumentu. 
	- Podvržená data v síťové komunikaci (man-in-the-middle). 
	- Proč je to problém: ztráta důvěryhodnosti dat.
## Detekce
- Redundance dat: 
	- Do dat se přidá něco navíc → kontrolní informace. 
	- Tyto kontrolní bity/slova se použijí ke zjištění, jestli data dorazila správně. 
	- Analogicky: „kontrolní číslice“ v rodném čísle nebo ISBN.
### Parita
- K řetězci bitů se přidá ==jeden bit== tak, aby byl celkový počet jedniček sudý nebo lichý. 
- Pokud se změní 1 bit → chyba se odhalí. 
- Pokud se změní 2 bity → chyba se nemusí poznat. 
- Sudá parita = počet jedniček je sudý např.: 1000110==1== 
- Lichá parita = počet jedniček je lichý např.: 1000110==0==
### kontrolní součet (checksum)
- Spočítá se součet všech bajtů (nebo jinak definovaná funkce). 
- Po přenosu se spočítá znovu → porovnání. 
- Používá se u souborů (např. při stahování – MD5/SHA hash).  
- 👉Ukázka: stáhnu soubor, zkontroluju hash na webu.
### CRC (cyclic redundancy check)
- Vypočítá se z dat polynomem. 
- Velmi spolehlivě odhalí chyby v blocích dat. 
- Použití: síťová komunikace (Ethernet, Wi-Fi), komprimované soubory (ZIP), QR kódy. 
- Důkladněji vysvětlené je to třeba na [wikipedii](https://cs.wikipedia.org/wiki/Cyklick%C3%BD_redundantn%C3%AD_sou%C4%8Det).
### Hashovací funkce
- Krátký „otisk“ dat. 
- Pokud se změní jediný bit, hash bude úplně jiný. 
- Použití: ověřování integrity souborů, hesla, digitální podpisy.
### Shrnutí a porovnání
- Parita – jednoduché, ale odhalí jen část chyb. 
- Kontrolní součet – lepší, odhalí víc chyb. 
- CRC – spolehlivé pro komunikaci. 
- Hash – spíš pro ověřování celistvosti, ne pro opravu.
## Oprava chyb
- Detekce chyby = systém pozná, že data nejsou správná (např. kontrolní součet nesedí). 
- Oprava chyby = systém nejen pozná, že je chyba, ale dokáže i zjistit, kde je a spravit ji. 
- Přirovnání: 
	- Detekce = víš, že diktát má chybu.  
	- Oprava = víš, kde přesně je a jak ji opravit.
### Jednoduché metody opravy
- Opakování zprávy: 
	- Data se pošlou vícekrát (např. 3×) → příjemce většinovým hlasováním určí správnou hodnotu. 
	- Nevýhoda: velká režie (víc dat). 
- Re-request (ARQ – Automatic Repeat reQuest): 
	- Pokud se zjistí chyba, příjemce si vyžádá znovu poslání. 
	- Používá se např. v protokolu TCP.
### Opravné kódy
- Do dat se přidá více kontrolních bitů než jen parita. 
- Umožní lokalizovat chybu a opravit ji. 
- Např.: 
	- Hammingův kód 
	- Reed-Solomon kódy (CD/DVD nebo QR kód)

[[Kódování dat]] 