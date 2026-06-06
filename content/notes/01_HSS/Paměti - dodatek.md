---
date: 2025-12-07
---
# Paměti
- Slouží k uchování informace binárně 
- Množství informací, které se dá do paměti uložit - kapacita paměti (B) 
## Základní obecné charakteristiky 
- Kapacita – kolik dat je možné uložit  
- Přístupová doba – doba čekání na splnění požadavku (rozlišujeme čtení/zápis), úzce souvisí se šířkou datové sběrnice 
- Přenosová rychlost – kolik dat je možné přečíst /zapsat za danou časovou jednotku; rychlost čtení>rychlost zápisu 
- Způsob připojení paměti k jiným zařízením 
- Cena/bit, případně cena/byte 
- - závislost obsahu paměti na napájecím napětí - zda se informace po vypnutí napájení ztratí 
## Operační (vnitřní) paměť obecný popis 
- obvykle přímo připojené k základní desce PC 
- skládá se z integrovaných obvodů a může být součástí nejen základních desek, ale i některých přídavných karet (GK) anebo zařízení (tiskárny) 
- Podle přístupu k údajům dělíme operační paměti na: 
	- RAM (Random Access Memory) - pamět s libovolným přístupem 
	- SAM (Sequential Access Memory) - paměť se sekvenčním přístupem (data jsou ukládána a čtena v pevném pořadí) 
## ROM 
- Energeticky nezávislá 
- Podtypy 
### 1. PROM (programmable ROM) 
- Další generace ROM pamětí 
- Je programovatelná, tedy jednou je možné provést zápis 
- Po prvním zápisu funguje jako klasická ROM 
### 2. EPROM (Erasable PROM) 
- lze opakovaně programovat, před každým programováním se však musí obsah paměti vymazat pomocí UV záření (někdy stačí slunce) 
- Opakující programování způsobuje degradaci paměti 
### 3. EEPROM (Electrically EPROM) 
- Vymazatelná elektrickými impulsy (téměř okamžitě) 
- Počet programování a mazání však bývá omezen 
### 4. Flash PROM/Flash EEPROM 
- mžiková paměť (rychlejší, než předešlé typy) 
- Opět se přeprogramováním ničí a dochází k degradaci 
- Kvalitnější EEPROM čipy zvládají 10 až 100 tisíc zápisů a mazání 
- Flash PROM čipy - Kód BIOS






## RAM 
- Hlavní pracovní paměť 
- Eneregeticky závislá 
- Každá buňka napájena jedním vodičem ve svislém směru a 1 ve vodorovném směru 
- Čím větší paměť máme k dispozici, tím je práce s počítačem plynulejší. V případě menší RAM se údaje často ukládají a čtou z disku, což zpomaluje práci a nutí procesor zbytečně čekat 
- Refresh prováděn řadičem paměti - Northbridge - sběrnice FSB 
- Několik typů DRAM: 
	- FPM- RAM – Fast Page mode 
	- EDO – RAM – extended datat output 
	- SDRAM – synchronous DRAM 
		- DDR SDRAM 
### SDRAM 
- Přenáší data pouze po náběžné hraně řídícího signálu systémového časovače 
- Dva bezpečnostní zámky 
- SIPP – do patice na základní desku 
####  DDR 
- Každá varianta má jinde umístěný zámek 
- Vycházejí z SDRAM - výroba poměrně levná 
- Přenášejí data na obou hranách (náběžně i sestupně) řídícího impulsu 
- Typy pamětí typu DIMM 
##### DDR SDRAM
- (doubledatarate Synchronous dynamic random access memory) 
- 184 pinů, šířka sběrnice 64 bitů 
- Napětí 2,5 – 2,6V 
##### DDR2 SDRAM 
- 240 pinů, šířka datové sběrnice - 64 bitů 
- Napětí 1,8 V
##### DDR3 SDRAM 
- 240 pinů, šířka datové sběrnice - 64 bitů 
- napětí 1,5/1,35V 
- technologie DDR3 se používá pro vysokorychlostní ukládání pracovních dat 
- Nejvyšší rychlost DDR2 – 1,2GHz, nejvyšší rychlost DDR3 – 2,4GHz 
##### DDR4 SDRAM 
- 288 pinů 
- Přímý nástupce DDR3 
- Na trhu poprvé v 2014 
- Piny DIMM 284, So-DIMM 256, frekvence cca 4,2GHz 
- Napětí 1,2/1,05V
##### DDR5 SDRAM 
- 288 pinů 
- na trhu v 2020 
- napětí 1,1V 
- Frekvence 6,4GHz 
### SO-DIMM
- (small outline dual in-line memory module) 
- Menší alternativa k DIMM 
-  V noteboocích a zařízeních s omezeným prostorem 
- Počet pinů závisí na typu paměti 
- Vzhledově se liší postavením výřezů 
### Frekvence aka rychlost RAM 
- Parametr definující rychlost 
- rychlost=frekvence x šířka sběrnice 
133MHz x 32 bitů = 4 256 Mb/s = 532MB/s

[[Paměti|předchozí]] [[SSD|následující]] 