---
date: 2026-02-06
---
# SSD 
- (solid state drive)
- (polovodičový disk) 
- Elektronický způsob ukládání (paměťové čipy) 
- Není napěťově závislá paměť 
- **Výhody**
	- nižší spotřeba energie 
	- nízká hmotnost 
	- vyšší spolehlivost (žádné pohyblivé části) 
	- tichý chod 
	- vyšší přenosová rychlost 
- **Nevýhody** 
	- Vyšší cena 
	- Horší poměr cena/kapacita 
----
## Formát SSD disků 
### M.2 
- moderní formát 
- Je v podobě rozšiřující karty, která se umisťují přímo na základovku 
### 2,5” 
- tradiční formát 
- Přejatý od plotnových disků
- Nejsou drahé a hodí se do starších sestav, připojují se přes SATA III
- Moderní způsob připojení - port U.2
### PCIe
- rozšiřující karta 
- Připojení skrz PCIe x4 (využívají standartní NVMe řadiče)
- Pro m.2 disky lze zakoupit redukční adaptér pro PCIe
----
## Rozhraní
### 1. SATA, MSATA 
- Nejstarší rozhraní 
- Nejlevnější 
- Nejrozšířenější 
### 2. PCIe
- Společně s M.2 nejrychlejší možností pro připojení SSD 
- Dražší 
- Základová deska musí obsahovat PCIe slot 
### 3. U.2
- Dokáže připojit 2,5” SSD pomocí standardu NVMe
- Vysoké rychlosti
- Lze připojit do slotu M.2 přes redukci
### 4. M.2
- Nejmodernější
- Používá několik typů sběrnic (PCIe 3.0, PCIe 4.0, SATA 3.0 A USB 3.0)
- Vlastní tvar i konektor
### NVMe
- (non-Volatile Memory express)  
- Specifikace rozhraní pro komunikaci mezi Flash pamětí a jejím řadičem 
- Vysokorychlostní paralelní přenos dat skrze PCIe sběrnici 
- Princip funkce: 
	- Tvořené tištěným spojem s ovládací elektronikou a NAND flash paměťovými čipy 
	- NAND flash udrží uložený stav i při vypnutém napájení 
	- Stejný typ pamětí ve všech moderních přístrojích
	- Modul NAND flash pamětí - tvořen velkým množstvím paměťových buněk představovaných jednotlivými tranzistory - sekvenční přístup
----
## SLC,MLC,TLC,QLC
### SLC (single level cell)
- schopné uložit do každé paměťové buňky 1 bit informací 
- může nabít pouze dva různé stavy (1 - prázdná, 0 - naprogramována) 
### MLC (multi level cell)
- Ukládají se 2 bity, 01; 02; 03; 04 
### TLC  (triple level cell)  
- Rozpozná 8 úrovní napětí, ukládají do paměťové buňky 3 bity 
- Levnější - nevydrží tolik 
### QLC  (Quad level cell) 
- Rozpoznává 16 úrovní napětí, do paměťové buňky se ukládají 4 bity 
---
## Wear levelling 
- rovnoměrné opotřebení SSD disků
### Opotřebení paměťových buněk 
- Míru opotřebení vyjadřuje zkratka TBW (terabytes written)

[[Paměti - dodatek|předchozí]] [[HDD|následující]]