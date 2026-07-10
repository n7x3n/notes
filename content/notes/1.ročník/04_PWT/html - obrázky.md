---
date: 2026-02-01
author: n7x3n
---
# Obrázky
- 6 hlavních faktorů
	1. formát (jpeg, gif, png, svg, WebP, AVIF)
	2. barva - zápis barev:
		- rgb (např. 120,100,180)
		- šestnáctkový (#0000ff)
	3. velikost a rozlišení
	4. datový objem (rychlost načítání/stahování)
		- používání komprese, vektorů (nevhodné pro fotky),
		- omezení rozměru
	5. průhlednost
	6. animace
## vložení obrázku na stránku
```html
<img src="obrazky/obrazek.jpg">
```
### atributy pro img

| atribut | význam                             | hodnoty |
| ------- | ---------------------------------- | ------- |
| src     | umístění souboru                   | URL     |
| alt     | alternativní popis                 | text    |
| title   | text, zobrazuje se po najetí myší  | text    |
| lowsrc  | náhradní obrázek pro malé displeje | URL     |
## favicon
```html
<link rel="shortcut icon" href="cesta-k-souboru" type="image/x-icon">
```
- psát do elementu <<code>head</code>> 

[[Odkazy v html|předchozí]] [[CSS-teorie|následující]]