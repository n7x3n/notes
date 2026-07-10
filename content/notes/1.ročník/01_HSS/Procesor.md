---
date: 2025-11-21
author: n7x3n
---
# Procesor
- CPU (central processing unit)
- Výkon celého počítače (do značné míry)
- Umístěn na základní desce počítače
- Patice, socket, či slot
	- Pin grid array (PGA)
		- Piny jsou uspořádány do pole tak, aby souhlasily s otvory v patici
	- Land grid array (LGA)
		- Dotyk kontaktních plošek
-  Ball grid array (BGA)
	- Připájeno přímo na základní desku

## Parametry ovlivňující výkon
### Vnitřní šířka dat
- popisuje schopnost procesoru zpracovat najednou množství dat
- čím více dat, tím je rychlejší
- 32-bitové, 64-bitové, 32 i 64-bitové
### Patice (socket)
- slouží k připojení procesoru k zákl. Desce
- různé typy procesorů - různé patice (dáno výrobcem procesoru)
### Jádro procesoru
- jádrem každého mikroprocesoru je logický obvod
- dokáže zpracovat sadu jednoduchých mikroinstrukcí
- mikroinstrukce – pouze jednoduché příkazy
- převod instrukční sady na mikroinstrukce obstarává program
- Více jader procesoru- zapojení více jednojádrových
	- jádro= samostatná výpočetní jednotka
- Jádra jsou na sobě výpočetně nezávislá- procesor schopen v jednu chvíli zpracovávat několik programů najednou – multitasking

### Hyper- threading
- technologie
- umožňuje aby 1 fyzické jádro zpracovávalo 2 vlákna (o těchto procesorových vláknech se mluví jako o virtuálních nebo logických jádrech)
- Z pohledu OS se instrukce dělí na vlákna, která se zpracovávají paralelně vůči sobě
- Fyzická jádra lze tedy dělit na virtuální jádra - procesor se 4 fyzickými jádry může obsahovat 8 virtuálních jader
- Nemůžeme tvrdit, že 2 jádrový procesor se 4 virtuálními jádry se vyrovná plnohodnotnému 4 jádrovému procesoru
## Další parametry CPU
### výrobní technologie
- uvádí se v nanometrech
- informuje nás, jakou nejmenší součástku v procesoru je firma schopna vyrobit (např. 32nm)
### frekvence procesoru
- Kolik operací vykoná procesor za 1 sekundu 
- uváděno v GHz (např. 2,93 GHz)
- čas, za který je procesor schopen přepnout tranzistory do jedničky a poté nuly - ==Frekvenční cyklus
- Množství cyklů - ==frekvence procesoru==
	- jednotka Hertz
- také označována názvy takt nebo kmitočet procesoru
- Jeden z hlavních faktorů, které ovlivňují výkon
- Čím vyšší frekvence, tím vyšší výkon (brát s rezervou)
- Celkový výkon ovlivňují i jiné faktory - např. Architektura, počet jader aj.
- typy frekvence
	- Vnitřní frekvence - čím vyšší, tím je procesor rychlejší
	- Vnější frekvence - určuje rytmus práce periferních zařízení a čipových sad na základní desce. Pracují pomaleji, než mikroprocesor

### taktování procesoru
- proces zvyšování ale i snižování výsledné frekvence
- Rovná se součinu základního taktu (BCLK) a hodnoty frekvenčního násobič procesoru
- BCLK (baseclock) - frekvence generovaná oscilátorem na základní desce
	- Krom procesoru ovlivňuje také řadu dalších frekvencí, např. Tak pamětí
- Frekvenci je ve většině případů možné ovlivnit
    - Změnou BCLK – z důvodu snížené stability často nedoporučuje a mnoho základovek touto možností nedisponuje
    - Úpravou hodnoty násobiče
- Používá se násobička, která z pomalejší vnější frekvence udělá větší frekvenci vnitřní, vnitřní je násobkem vnější frekvence
### Cache procesoru (L1, L2, L3)
- česky vyrovnávací paměť
- vyrovnávají rychlostní rozdíly mezi jednotlivými komponentami
- Velmi rychlé
- V procesoru se dělí podle vrstev (ang. Layer) - proto písmeno L před - číslovkou vrstvy
- L3 cache - nejpomalejší, nejobjemnější a sdílí všechna jádra;
	- čím je úroveň nižší, tím menší je její objem, vyšší její rychlost a zároveň má blíže k procesoru
- Paměti L2 a L1 implementovány přímo v jádře
- Čím větší paměť L3 cache, tím lépe
### TDP procesoru 
- (thermal Design Power)
- maximální tepelný výkon procesoru 
- množství tepla, které při svém maximálním zatížení může produkovat
- parametr používaný především ve spojení s dimenzováním chlazení 
- jedná se spíše o teplotní strop, než střední teplotu
- chlazení se dělí na
	- aktivní - ventilátor
	- pasivní- hliníková žebra
	- kombinované - na hliníková žebra je připojen ventilátor - __Nejlepší způsob__
## Stavy procesu
- životní cyklus procesu
- prochází jednotlivými stavy
	- new – proces se vytváří
	- running state- proces je právě vykonáván
	- Ready state . Proces by mohly být vykonáván, kdyby byl proces právě volný, stojí ve frontě
	- Blocked state či waiting – proce čeká až nastane nějaká událost, po které by mohl pokračovat
	- Terminated – proces byl ukončen
- OS udržuje aktualiovaný seznam připravených a seznam blok. Procesů
### Pipeline (instrukční kanál)
- Fáze zpracování rozděleny na několik kroků
- Počet kroků závisí na interním návrhu procesu
	- Instruction fetch - vyzvednutí instrukce
	- Decode - dekódování instrukce
	- Execute- provedení instrukce
	- Memory access - přístup paměti (čtení/zápis)
	- Commit (writeback) - zápis výsledku

#### subskalární (sekvenční) zpracování
- každá část CPU může zpracovávat jednu instrukci v určité fázi
- Problémy instrukčních kanálů
	- Pipeline stall - zpoždění zpracování
	- Pipeline flush- vyprázdnění
## procesory v číslech

- Průměrná plocha čipu: 1cm čtverečný
- Průměrný počet čipů na waferu: 600
- Náklady na výrobu 1 procesoru: cca. 70-200 dolarů
- Podíl procesorů na trhu
    - - 70-75% intel
        - 30-25% AMD
        - 1% ostatní (VIA)

[[Sběrnice a sloty|předchozí]] [[Paměti|následující]] 