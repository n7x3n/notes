---
date: 2025-12-09
---
# Formátování textu
- **Nadpisy**
	- <code>h1 - h6</code>
	- <code>hgroup</code> - seskupení nadpisů
- holý text - base font - obvykle Times New Roman ignorující řádkování - jinak element <code>p</code>
- **Zalomení řádku** -<code> br</code> - break; pouze v případě, že je nutné zalomit řádku např. u básniček
## Fyzické formátování
- říká, jak má text vypadat
- nezabývá se logickou rolí formátovaného textu (kromě sup a sub)

### Tagy fyzického formátování textu

| Tag | Význam          | Párový | specifikace |
| --- | --------------- | ------ | ----------- |
| b   | tučné písmo     | ano    | jen v HTML  |
| i   | kurzíva         | ano    | jen v HTML  |
| u   | podtržení textu | ano    | jen v HTML  |
| sub | dolní index     | ano    |             |
| sup | horní index     | ano    |             |
## Logické formátování
- také nazývané idiomy (frázové prvky)
- vymezují význam elementu - přidávají textu strukturální informaci
### Tagy logického formátování textu

| Tag     | Význam               | Párový | Obvyklý vzhled |
| ------- | -------------------- | ------ | -------------- |
| span    | úsek textu           | ano    | normální       |
| strong  | zvýraznění (tučně)   | ano    | tučné          |
| em      | zvýraznění (kurzíva) | ano    | kurzíva        |
| cite    | citace               | ano    | kurzíva        |
| code    | výpis kódu           | ano    | strojopis      |
| dfn     | nově použitý termín  | ano    | kurzíva        |
| kbd     | vstup z klávesnice   | ano    | strojopis      |
| samp    | ukázka               | ano    | strojopis      |
| var     | formátování proměnné | ano    | kurzíva        |
| abbr    | ustálený výraz       | ano    | normální       |
| acronym | zkratka              | ano    | normální       |
| del     | smazaný obsah        | ano    | přeškrtnuto    |
| ins     | přidaný text         | ano    | podtrženo      |
| q       | citace               | ano    | normální       |
### Zvýraznění
- silné zvýraznění - element <code>strong</code> - bude vykreslen tučně
- obyčejné zvýraznění - element <code>em</code> - emphasis, vykreslené kurzívou
### Citace a reference
- **element <code><b>cite</b></code>** - citace nebo reference zdroje - např. jméno osoby, firmy, hry, knihy, písně atd.; vykreslen kurzívou
- dva speciální elementy pro označování citovaného textu ze zdroje
	- **Element** <code><b>q</b></code> - krátká citace - vykreslen v uvozovkách
	- **Element** <code><b>blockquote</b></code> - samostatná (většinou delší) citace, je blokový, 
### Zkratky a reference
- **Element** <code><b>abbr</b></code> - zkratky, které se čtou po písmenech, např. DVD, VHS
- **Element** <code><b>acronym</b></code> - zkratky, které čteme jako jedno slovo - např. AIDS
- oba elementy je možné doplnit o atribut <code><b>title</b></code>, který může obsahovat definici
- **Element** <code><b>dfn</b></code> - definice nového výrazu
### Práce s programy
- **Element** <code><b>code</b></code> - zápis zdrojových kódů, vykreslen neproporcionálním písmem
- **Element** <code><b>var</b></code> - proměnné
- **Element** <code><b>samp</b></code> - výstup programu (ukázka), vykreslen neproporcionálním písmem
- **Element** <code><b>kbd</b></code> - text, který má být zadán návštěvníkem, např. <kbd>ctrl+c</kbd> 
### Horní a dolní index
- **Element** <code><b>sup</b></code> - např. h<sup>4</sup> 
- **Element** <code><b>sub</b></code> - např. b<sub>6</sub> 
- hlavně v situacích, kde jsou nezbytně nutné
- neměly by sloužit jako okrasné elementy
### Horizontální oddělení
- **Element** <code><b>hr</b></code> - prázdný, nepárový, oddělení jednotlivých částí dokumentu
- prohlížeč ji vykreslí jako horizontální linku
- (hr jako hard line)
### změny dokumentu
- **Element** <code><b>del</b></code> - zrušená část dokumentu, např. <del>donést knížku</del> 
- **Element** <code><b>ins</b></code> - označuje nově vložený obsah
- oběma je možné přiřadit atribut <code>cite</code>, který vysvětluje důvod změny a atribut <code>datetime</code> obsahující datum změny. Důvod změny může být obsažen v atributu <code>title</code>. Atribut <code>datetime</code> obsahuje datum a čas změny ve formátu ISO
### Element pre
- dodržuje formátování obsahu - správně interpretuje zakončení řádku klávesou enter a libovolný počet mezer
### Další elementy
- <code><b>wbr, ruby, rp, rt, bdi, bdo, meter, progress</b></code>
- minimální využití

- <code>small</code> - malé písmo na okraj, např copyright

[[Odkazy v html|následující]] 