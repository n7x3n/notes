---
date: 2025-11-18
author: n7x3n
---
# Dělení programovacích jazyků

![[Dělení programovacích jazyků.png]]

## Nižší jazyky
- [[#1.generace]] a [[#2.generace]]
- Strojově orientované
- příkazy jazyka=instrukce procesoru
- výhody- rychlost programu
- nevýhody- náročnost pro lidi, složité programování, nepřehlednost, napsané pro konkrétní procesor
- moc se nepoužívají
- rychlé programy pro jednočipy, psaní jader operačních systémů atd.
## Vyšší jazyky (formální jazyky)
- [[#3.generace]], [[#4. generace]] a [[#5.generace]]
- většina jazyků
- orientace na člověka
- zapisuje se strukturovaně = srozumitelný zápis
- není tak závislý na procesoru
### Procedurální/imperativní/příkazové
- Hlavně 3. a 4. generace
- programátor zadává příkazy jeden za druhým
#### Sekvenční
- [[#3.generace]]
- posloupnost příkazů, cykly, větvení (podmínky)
- např. Cobol, Pascal, C, Basic
#### Objektově orientované - OOP
- [[#3,5. generace]] a [[#4. generace]]
- používají se objekty (data+metody) a vztahy mezi nimi
- důležité pojmy OOp - zapouzdření, polymorfismus, dědičnost, abstrakce
- např. C++, Java, JavaScript, Python
## Neprocedurální/neimperativní/deklarativní
- [[#5.generace]]
- není pevná struktura programu
- definována pravidla a mantinely programu
- programy 5. generace
### funkcionální
- program je množina, ale není to posloupnost
- většinou neexistují proměnné, ale jen seznamy dat
- např. Lisp
### logické
- množina pravidel a odvozovacích pravidel
- znají proměnné
- využívají se hlavně v AI

# Vývoj programovacích jazyků
## 1.generace
- strojový kód
- Nejstarší typ programovacího jazyka
- instrukce jsou tvořeny posloupnosti nul jedniček (bitů)
- hardwarově závislý
- obtížné hledání chyb
- jednoúčelové programy, obvykle s využitím v matematice a fyzice
- IBM System 370 strojový kód
	00000011 00001011 00100100 01000011  
	00001010 00000011 00000011 00000011  
	00000011 00000010 00000011 00001001  
	00000111 00000011 00001001 00000011  
	00000011 00000011 00000011 00010100  
	00000011 00000011 00000011 00000011
## 2.generace
- jazyk symbolických adres (Assembler)
- jazyk nižší úrovně
- obecné příkazy (např. "načti data", "zapiš data") jsou zkracovány pomocí symbolických názvů
- příkazy překládá do strojového kódu procesoru speciální program - assembler
- také hardwarově závislý
- IBM System 370 assembler
	L R2, = F’2’
	A R2, = F’5’
	ST R2, Y
## 3.generace
- procedurální jazyky
- Vyšší úroveň programování (podoba s lidskými jazyky)
- Příkazy odvozené z anglických slov
- programátor zapisuje zdrojový kód; překladač provede interpretaci nebo překlad do strojového kódu (strojového jazyka)
- Koncepce strukturovaného programování
- Jazyky: Fortran, Cobol, C, Pascal, Basic
	- Fortran
		Y=2+5
	- Cobol
		add 2, 5 giving y
	- Basic
		let y=2+5; 
	- C
		y=2+5;
## 3,5. generace
- Objektově orientované jazyky (OOP)
- někde uváděny jako 3½. generace, někdy jako 4.generace
## 4. generace
- problémově orientované jazyky
- vyšší úroveň programovací jazyků
- mnoho vestavěných funkcí, bývají často napojeny na databázi
- snaha o zjednodušení a zrychlení práce programátora
- jazyky: C++, Java, ...
	- Python
		y=2+5
## 5.generace
- přirozené jazyky
- neprocedurální programování
- počítači neříkáme, jak dojde k cíli, ale jaká pravidla má použít
- nadefinujeme objekty, pravidla, omezení, kritéria kterým musí řešení vyhovovat
- počítač sám hledá způsob dosažení
- klíčový pojem: rekurze
- Jazyky: Prolog, Lisp, Clojure
	- Lisp
		(+ 2 5)

[[Algoritmus|předchozí]]     [[Data a datové struktury|následující]] 