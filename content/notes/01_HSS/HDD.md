---
date: 2026-02-27
---
# HDD 
- Vysokokapacitní médium
- Princip: rotující magnetický disk
- Využívá magnetizace materiálu a pracuje s 2 stavy informace – 0 a 1
- Zápis a čtení dat probíhá pomocí magnetické indukce 
## Parametry 
- **Kapacita** – kolik dat je možno uložit 
- **Otáčky** - rychlost otáčení kruhových desek (ploten) na kterých jsou uložena data 
	- (5400, 5900 ot/min; 7200 ot/min; serverové 10-15000 ot/min apod.) 
- **rychlost čtení** - kolik dat za sekund přečte
- **rychlost zápisu** - kolik dat za sekundu uloží 
- **rozhraní** - pro připojení 
- **Vyrovnávací paměť (cache)**
	- součástí pevného disku 
	- Dočasné ukládání dat 
	- Účel - zrychlení přístupu k datům a optimalizace přenosu 
	- Paměť typu SRAM 
## Rozhraní pro připojení 
### 1) EIDE (ATA, PATA) 
- starší typ rozhraní 
- paralelní 
- max. 2 HDD 
### 2) SATA 
- přenáší data sériově 
- rychlejší než EIDE 
- Hot swap 
### 3) SCSI 
- nejrychlejší 
- u serverů 
- na 1 rozhraní lze připojit více HDD 
## zákl. Součásti 
- Plotny disku 
- Hlavy pro čtení 
- Pohon hlav 
- Pohon ploten disku 
- Vzduchové filtry 
- Řídící deska s elektronikou 
- Kabely 
- Konektory 
- Další konfigurační prvky (např. Propojky a přepínače)
![[hdd-soucasti.jpg]]
### Plotny 
- Klasický pevný disk – 1 nebo více ploten 
- Materiál: Kov nebo sklokeramika 
- V současné době nejčastěji používané disky (velikost udávaná v palcích, průměr plotny)
#### “3.5” - 95 mm
- u stolních pc 
#### “2.5” - 65 mm
- přenosné pc 
#### “1” - 34 mm
- tzv. Microdrive 
### Hlavy pro čtení a zápis 
- Pro každý povrch plotny má disk elektromagnetickou čtecí a zápisovou hlavu s **mikroskopickou cívkou** 
- Plotny se točí konstantní rychlostí (od 3600 do 15000 otáček za minutu) -> vytváří se tenká vzduchová vrstva, na níž se hlavy pohybují 
### Pohon hlav a pohon ploten 
#### pohon ploten 
- Miniaturní motor pro otáčení ploten disku 
- Vždy připojen přímo k hřídeli otáčející plotnami disku 
- Motory nesmí produkovat vibrace 
- Rychlost otáček nastavena automaticky – nelze ji měnit 
- Je těsně pod plotnami, nebo vestavěný do hřídele 
#### pohon hlav 
- Elektromagnetický 
- Použita ve všech discích pro její vyšší přesnost 
## Princip funkce HDD 
- HDD je složeno z několika ploten, které jsou umístěny nad sebou 
- Mezi jednotlivými plotnami jsou po obou stranách elektromagnetické hlavy - záznam a čtení dat 
- Čtecí hlava při otáčení disku dosáhne na libovolné místo plotny 
- **Disku se přímo nedotýká** 
- Pohyb ramene s čtecí hlavou zajišťuje přesná mechanika, kterou řídí **řadič disku** 
### Záznam dat 
- Provádí se pomocí hlavy pro čtení a zápis 
- Hlava pluje vlivem otáčení disku na vzduchovém polštáři a nikdy se nesmí dotknout povrchu disku (mechanické poškození) 
- Při zápisu prochází proud cívkou, která vytváří magnetické pole 
- Magnetické pole je vedeno přes jádro cívky k magnetickému povrchu plotny
- Feromagnetické částečky na povrchu plotny se chovají jako trvalé magnety
- Pokud cívkou prochází elektrický proud, dojde k vytvoření určitého magnetického toku
- V závislosti jakým směrem při této operaci teče proud můžeme tvořit magnetická místa, která budou zmagnetizována tím či oným směrem 
### čtení dat 
1. Vystavení čtecích hlav na příslušný cylindr pomocí krokového motorku (dříve) nebo elektromagnetu (dnes) 
2. Pootočení disku na patřičné sektory 
3. Načtení dat
- Aby čtení probíhalo rychle a přesně, jsou kotouče disku logicky rozděleny na stopy a sektory
- Stopy rozděleny na kružnice na disku a ty jsou rozděleny příčně na sektory
- Každá stopa i sektor očíslovány
- Pokud disk obsahuje více povrchů, všechny stopy stejného poloměru (přístupné bez pohybu čtecí hlavy) - nazývá se cylindr (válec)
- Orientace záznamové a čtecí hlavy mezi stopami a sektory ovládá tzv. Řadič disku
- Čtení založeno na principu elektromagnetického indukce
- V cívce se indukuje napětí při přechodu z 0 na 1 a z 1 na 0
![[hdd.png]]

[[SSD|předchozí]] [[Přídavné karty|následující]]