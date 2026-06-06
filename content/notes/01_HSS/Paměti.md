---
date: 2025-11-28
---
# Paměti
## Hierarchie pamětí
-  pyramida paměti
![[pyramida_paměti.png]]
### 1.Úroveň - registry procesoru
- malá, extrémně rychlá paměť umístěná v jádře CPU
- uchovávají operandy, instrukce a mezivýsledky
- přístupová doba odpovídá taktu procesoru
- v řádech bitů až stovek bajtů
- cpu přistupuje napřímo, bez sběrnice
### 2.Úroveň - cache (vyrovnávací paměť)
- L1(nejrychlejší); L2, L3 (sdílené pro jádra)
- mezi procesorem a operační pamětí
- vyrovnává obrovský rozdíl v rychlosti mezi super-rychlým CPU a pomalejší RAM
- princip: uchovává kopie data a instrukcí, které bude procesor pravděpodobně brzy potřebovat
- technologie: SRAM (static RAM) - rychlá, ale drahá
### 3.Úroveň - operační paměť RAM
- hlavní pracovní paměť počítače pro běžící programy a data
- energeticky závislá (volatile): po vypnutí napájení se data ztratí
- buňka tvořena kondenzátorem a tranzistorem
- vyžaduje tzv. Refresh (obnovovací náboje)
- typy: SDRAM, (DDR 1,2,3,4,5)
## SRAM vs. DRAM
### SRAM
- uchovává info po celou dobu připojení k napájení
- bistabilní klopný obvod (min. 2 tranzistory na buňku)
- vlastnosti:
	- bit je udržen dokud se nepřeruší napájení
	- krátká přístupová doba (velmi rychlá)
- použití: např. Cache (vyrovnávací paměť)
### DRAM
- Struktura: 1 tranzistor + 1 kondenzátor (nabití = 1 bit)
- refresh (oživování)
- náboj se v čase vybíjí - nutnost data pravidelně používat
	- při obnově nelze paměť používat
- čtení je destruktivní: přečtení vybije náboj - data se musí znovu zapsat (obnovit)
- zápis je rychlejší než čtení
- typy: SDRAM, DDR

#### SDRAM (synchronous DRAM)
- Synchronní: používá hodinový signál (běží v taktu s PC)
- Inteligence čipu: rozšířený protokol, automatická obnova dat
- Burst režim (dávkový přenos):
    - Inicializace adresy proběhne jen jednou
    - Poté se v každém taktu přenese jedna hodnota (blok dat)
#### DDR (double data rate)
- typ přenosu na sběrnici
- princip: lepší využití hodinového signálu
- funkce:
	- využívá vzestupnou i sestupnou hranu signálu
	- vyslány dva signály (data) za jeden hodinový takt
#### Paměť ROM (Read only memory)
- Specifikum: paměť určená primárně pro čtení
- Energeticky nezávislá (data zůstávají i bez proudu)
- Uložení firmware (BIOS/UEFI) - startovací instrukce PC
- Vývoj technologií
    - ROM: zapsána při výrobě (nelze měřit)
    - PROM: lze jednou naprogramovat nebo mazat UV zářením (P- Programmable)
    - EPROM – mazatelná UV zářením
    - EEPROM/ Flash: Elektricky přepisovatelná (dnešní BIOSy, USB disky)


## 4. úroveň -  sekundární úložiště 
### (HDD) 
- [[HDD]] - hard disk drive
- klasický pevný disk 
- magnetický záznam dat na rotující plotny 
- data uložena ve stopách, sektorech a válcích (cylindrech) 
- čtecí hlavy se pohybují nad povrchem na vzduchovém polštáři 
- klady: vysoká kapacita za nízkou cenu 
- zápory: mechanické části (hlučnost, teplo, náchylnost k poškození), pomalejší 
### (SSD) 
- [[SSD]] – solid state drive - moderní náhrada HDD 
- technologie: ukládání dat do polovodičových čipů (NAND flash) 
- Výhody oproti HDD 
	- žádné pohyblivé části - tichý chod, vysoká odolnost 
	- výrazně vyšší přenosové rychlosti a minimální přístupová doba 
- Nevýhody: 
	- Vyšší cena za GB, omezený počet přepisů buněk 
- Wear levelling: technologie řadiče - rovnoměrné opotřebení buněk 
## 5. úroveň - terciální a externí paměti 
- archivace, zálohování, přenos dat, distribuce SW 
- Optická média: 
	- CD (infračervený laser), DVD (Červený), Blu-ray (Modrý) 
	- Lisované (ROM) vs. Vypalované (R/RW) 
- Flash paměti: USB klíčenky, paměťové karty 
- Magnetické pásky: Stále využívané pro levnou archivaci obrovských objemů dat v korporátní sféře (sekvenční přístup) 
## Virtuální paměť 
- Kombinace fyzické RAM a části disku (Swap/Pagefile) 
- OS vytváří iluzi velké souvislé paměti 
- Stránkování (paging): 
	- Paměť se dělí na bloky pevné velikosti (Rámce v RAM/Stránky ve virtuální) 
	- OS ve spolupráci s HW (MMU) přesouvá nepoužívané stránky na disk a uvolňuje 
# Shrnutí 
- Hierarchie je o kompromisu: Nelze mít paměť, která je zároveň obrovská, levná a super- rychlá 
- Tok dat v počítači 
	- 1. Data jsou trvale uložena na HDD/SSD 
	- 2. při spuštění programu se nahrají do RAM 
	- 3. Často používané instrukce se přesunou do Cache 
	- 4. Pro samotný výpočet jdou data do Registrů CPU 
- Správce paměti (OS) zajišťuje, aby tento proces uživatel vnímal co nejplynuleji

[[Procesor|předchozí]] [[Paměti - dodatek|následující]] 