---
date: 2025-11-25
---
# Data
## Data vs. Informace
vis. [[Informace x data]]
## Datové struktury
- Konkrétní způsob organizace dat v paměti počítače
- zajišťuje, aby mohla data být používána efektivně 
- umožňuje uchovávat a zpracovávat množinu dat stejného typu nebo různorodých, ale logicky souvisejících dat
### samostatné hodnoty vs. strukturované údaje
#### Samostatné hodnoty
- jednotlivé hodnoty, které nejsou spojeny žádnými jinými hodnotami
- obvykle používané pro jednoduché výpočty nebo porovnání
- např. Výsledek příkladu, okamžitá hodnota na digitální teploměru
#### Strukturovaná data
- Obvykle uspořádána do tabulek, záznamů, neboj jiných struktur, které umožňují snadné vyhledávání a manipulaci. 
- používané pro složitější úlohy, jako analýza dat a vytváření zpráv
- Např. Kontakt v telefonu, záznam v databázi
### Základní datové struktury vs. odvozené datové struktury
#### Základní datové struktury
- proměnná, pole, záznam a objekt 
- u většiny program. Jazyků, mají je nadefinované
#### Odvozené datové struktury
- Seznam, zásobník, fronta a strom 
- Musíme je nadefinovat, nebo použít knihovnu  
- Také známá jako abstraktní datové struktury
## Datový typ
- určuje u dat:
	- Obor hodnot - jestli je to číslo, písmeno, ano/ne 
	- Rozsah - jak velké číslo nebo kolik znaků 
	- Povolené operace - co s takovými daty můžu dělat
### Dynamicky typované jazyky
- Python, javascript, Lisp, Lua, PHP, Prolog, Ruby, Smalltalk 
- Nepožadují specifikaci datového typu u proměnných 
- pružnější - programy generují typy a funkcionalitu na základě běhových dat, ale častější běhové chyby
### Staticky typované jazyky
- Vyžadují deklaraci proměnné a její datový typ 
	- Výhoda: omezí se množství chyb 
	- Nevýhoda: zpětně nezměním
## Proměnná
- Pojmenované místo v paměti počítače 
- Je v ní uložena hodnota určitého datového typu 
- Vytvoří se na základě deklarace 
	- Její jméno (identifikátor)
	- Datový typ 
- Počítač zachází s proměnnou prostřednictvím její adresy
## Datové struktury
### Lineární datové struktury
#### Pole
- (ang. array)
- prvky uspořádány za sebou v jednom "řádku"
- pevná velikost - délka obvykle dána při vytvoření a nelze měnit později
- stejný datový typ - všechny prvky mají stejný typ (např. int, double, char)
- typické operace s polem:
	- přiřazení hodnoty do pole: pole [index] = hodnoty
	- čtení hodnoty z pole: hodnota = pole [index]
	- procházení pole

![[Pole - datová struktura.png]]
#### Seznam
- (ang. list)
- ukládání kolekce prvků v určitém pořadí
- vlastnosti
	- linearní struktura
	- dynamická velikost - může se libovolně zvětšovat nebo zmenšovat podle potřeby
	- prvky mohou být různého typu (záleží na implementaci - např. Pythonu ano, v Java seznamu s generikem ne)
	- umožňuje vkládání a mazání prvků bez nutnosti pevné velikosti
- typické operace seznamu
	- přidání prvku (append)
	- odebrání prvku (remove, pop)
	- přístup k prvku podle indexu (seznam [i])
	- průchod seznamem (for cyklus)
#### Fronta
- (ang. queue)
- funguje podle principu FIFO - *first in, first out* (první dovnitř, první ven)
- vlastnosti fronty
	- lineární struktura - řazeny v pořadí, v jakém byli vloženy 
	- prvky se vkládají na konec a odebírají se z jejího začátku
	- umožňuje spravedlivé zpracování požadavků, např. ve frontě na tisk nebo zprávy
- typické operace s frontou
	- enqueue - vložení prvku (např. append)
	- dequeue - odebrání prvku (např. popleft)
	- peek - nahlédnutí na první prvek (bez odebrání)
#### Zásobník
- (ang. stack)
- funguje podle principu LIFO - *Last in, first out* (poslední dovnitř, první ven)
- vlastnosti zásobníku
	- lineární struktura - prvky jsou vkládány na vrchol a odebírány také z vrcholu
	- prvky se vkládají a odebírají z jednoho konce (tzv. vrchol)
	- typické využití např. při rekurzi, zpracování výrazů, návratu zpět v aplikacích
- typické operace se zásobníkem
	- push - vložení prvku (např. append)
	- pop - odebrání posledního prvku
	- peek - nahlédnutí na vrchol zásobníku bez odebrání
### nelineární datové struktury
#### Strom
- nelineární datová struktura
- skládá se z uzlů (nodes)
- vytváří hierarchii, kde každý prvek (uzel) může mít více "podřízených" uzlů
- základní pojmy
	- kořen stromu (root) 
		- první (nejvyšší) uzel stromu, od kterého vše začíná
	- uzel (node) 
		- prvek stromu, který může obsahovat data a odkazy na další uzly
	- Hrana (edge) 
		- Spojení mezi dvěma uzly - vede od rodiče k potomkovi
	- List (leaf) 
		- Uzel, který nemá žádné potomky
	- Vrstvy stromu 
		- Úrovně stromu podle vzdálenosti od kořene. Kořen je ve vrstvě 0, jeho děti ve vrstvě 1 atd.
	- Výška stromu
		- Nejdelší cesta od kořene k listu, měřená v počtu hran.
- Speciální typy stromů
	- Binární strom 
		- Každý uzel může mít maximálně **dvě děti** – levé a pravé.
- Vyvážený strom
	- Strom, kde jsou podstromy u každého uzlu zhruba stejně vysoké –to zajišťuje efektivní vyhledávání, vkládání a mazání.
- stromy se často používají v databázích, při vyhledávání, v operačních systémech nebo při organizaci souborů (např. stromová struktura složek)

![[Strom.jpg]]

[[Dělení a vývoj jazyků|předchozí]]   [[poznámky z 10.2|následující]] 