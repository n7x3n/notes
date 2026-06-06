---
date: 2026-03-15
---

> [!TIP] Tip
> tabulka s váhou každého selektoru je [[#Specifičnost selektoru|tady]]

# Komentář
- komentář se zapisuje pomocí kombinace hvězdičky a lomítka
- hvězdička je vždycky psaná směrem dovnitř do komentáře
```css
/*komentář*/
```
# Styly
![[pwt-pravidlo.png]]

- **příklad**:
```css
p {color: blue; letter-spacing: 2px;}
```
- modrá barva textu a větší mezery mezi písmeny
## Druhy zápisu CSS
### 1. řádkový styl (aka přímý, inline)
- zapisují se rovnou do elementu
- váha 1000
- **příklady**:
```html
<p style="color: blue">Toto je text formátovaný pomocí CSS stylu.</p>
```
```html
<p style="color: blue; font-size: smaller">Toto je text vytvořený pomocí CSS stylu.</p>
```
- výhody:
	- přímo u prvku jde vidět jeho definice
	- výhodné pro dynamické změny ve spojení se skriptovacím jazykem
- nevýhody:
	- nepraktické - musí se vypisovat u každého prvku zvlášť
	- náročná údržba
### 2. Tabulky CSS (šablony)
#### A) Interní stylová tabulka
```html
<head>
<style type="text/css">
	body {font-family: Arial, Verdana,sans-serif; font-size: small;}
	p {width: 300px; border: 1px solid black;}
</style>
</head>
```
- výhody:
	- popis vzhledu je přímo v html
- nevýhody:
	- platí jen pro 1 stránku
	- náročnější údržba
#### B) Externí stylová tabulka
```html
<head>
	<link rel="stylesheet" href="styl.css"/>
</head>
```
- **rel** - určuje typ šablony; buď <code>stylesheet</code> - základní šablona, nebo <code>alternate</code> - alternativní šablona
- **href** - určuje URL adresu
- výhody:
	- lze použít 1 soubor se stylem pro celý web
	- snadná úprava vzhledu celého webu
	- úspora přenosové kapacity
- nevýhody:
	- prvotní načtení první stránky trvá trochu déle, později se styl "cachuje" - výhoda
#### C) externí stylová tabulka volaná z tabulky CSS
```css
@import url ("soubor.css")
```

![[schema-pripojeni-css.png]]

# Selektory
## Rozdělení selektorů
### 1. Typové selektory
- nejjednodušší varianta
- název selektoru je tvořen elementem html
- váha 1
- <code>element {deklarace vlastností;}</code>
```css
h1 {text-decoration: underline;}
p {color: blue; font-style:italic;}
```
### 2. pojmenované selektory
- html elementy se dají pojmenovat pomocí **třídy**, nebo **identifikátoru**
- názvy bez diakritiky, mezer a speciální znaky (např. otazník nebo vykřičník)
- název může být libovolný
#### A) Selektor třídy-class
- každý element může být zařazen do třídy, nebo víc tříd současně
- <code>.třída {deklarace vlastností;}</code>
- **příklady**
```css
.vyrazny {color: red;}
```
- provede se na každý prvek se třídou <code>vyrazny</code>
- pokud chceme tuto třídu použít jenom na určitý element:
```css
h1.vyrazny {color: red;}
```
- <code>element.třída {deklarace vlastnosti;}</code>
- **Přiřadění třídy k nadpisu**:
```html
<h1 class="vyrazny">Hlavní nadpis</h1>
```
#### B) Vícenásobné třídy
- v css:
```css
.vyrazny {color: red;}
.novinka {background-color: yellow}
```
- v html:
```html
<p class="novinka vyrazny">Text třetího odstavce</p>
```
#### C) Selektor identifikátoru
- vyšší priorita než třída
- vyskytuje je se jenom v 1 elementu
- v css se vyvolává pomocí hashtagu
```css
#vyrazny {color: red;}
```
- do html prvku pak v podobě atributu <code>id</code>
```html
<p id="vyrazny">Červený odstavec</p>
```
### 3. Univerzální selektor
- vztahuje se na všechny elementy
- nejslabší (váha 0000)
- <code>* {deklarace vlastností;}</code>
```css
* {text-decoration: underline;}
```
### 4. Selektor potomka (dítěte)
- píše se: <code> rodič potomek {deklarace vlastností;}</code>
- vztahuje se na všechny potomky
- **selektor dítěte** má syntaxi: <code>rodič>dítě {deklarace vlastností;}</code>
- vztahuje se jenom na přímé potomky -> kdyby byly další vnořené elementy, tak se už nemění
### 5. Selektor sousedících sourozenců
- <code>element1 + element2 {deklarace vlastností;}</code>
- formátuje pouze <code>element2</code>
- elementy musí být vedle sebe (ne v sobě vnořené) a musí být hned za sebou
- musí mít stejného rodiče
- **Příklad**:
```css
h1 + p {text-indent: 0;}
```
- v tomto případě se styl použije na první odstavec přímo za <code>h1</code>
### 6. Selektor obecných sourozenců
- <code>element1 ~ element2 {deklarace vlastností;}</code>
- funguje podobně jako selektor sousedících sourozenců ale s jednou zásadní změnou: **elementy nemusí stát přímo za sebou a pravidlo se vztahuje na všechny sourozence**
- **příklad**:
```css
h3 ~ p {font-size: 80%;}
```
- styl se použije na všechny odstavce, které jsou za <code>h3</code>, které mají stejného rodiče
- styl se nepoužije na žádný odstavec obsažený v kódu dříve než <code>h3</code>
### 7. Selektor parametrů (atributů)
- využívají atributů, které už jsou v html elementech
- má několik různých podob (v následujícím výpisu nejsou všechny):
	1. <code>element[parametr] {deklarace vlastností;}</code> -> tohle vybere element s určitým parametrem, bez ohledu na hodnotu uvnitř toho parametru
	2. <code>element[parametr=hodnota] {deklarace vlastností;}</code> -> tohle vybere element s parametrem, který má určitou hodnotu
	3. <code>element[parametr~=hodnota] {deklarace vlastností;}</code> -> tohle vybere element, u kterého je parametr, jehož součástí je také hodnota napsaná v pravidlu - v podstatě tomu říkáš: "podívej se do parametru u tohohle prvku a když tam najdeš tuhle hodnotu, tak ten element naformátuj"
	4. <code>element[parametr|=hodnota] {deklarace vlastností;}</code> -> v tomhle je důležitý symbol |, který říká, že hodnota v parametru musí buď být identická s hodnotou v pravidlu, nebo začíná tímto slovem následovaným pomlčkou
	5. <code>element[parametr1] [parametr2] {deklarace vlastností;}</code> -> vybere element s těmito parametry
## Pseudoprvky a pseudotřídy
- závisí na informacích, které se získávají až po načtení HTML dokumentu
- popisují prvky, které jsou v nějakém stavu
- před jejich název se používá dvojtečka
- **Váha**: 
	- pseudotřídy - 0010
	- pseudoelementy - 0001

| pseudotřída | význam                                       |
| ----------- | -------------------------------------------- |
| :hover      | prvek má tuhle třídu, když je nad ním kurzor |
| :active     | aktivovaný prvek (zrovna se na něj kliklo)   |
| :link       | nenavštívený odkaz                           |
| :visited    | navštívený odkaz                             |

| pseudoelement  | význam                   |
| -------------- | ------------------------ |
| ::first-line   | první řádek texu v prvku |
| ::first-letter | první znak textu v prvku |

---
# Specifičnost, Dědičnost, Kaskáda
- všechny tři slouží pro vyřešení případu, že se 1 element snaží stylovat více pravidel
- **Specifičnost** 
	- určuje váhu
	- sčítá body jednotlivých druhů selektorů
	- silnější vždy přebije slabší
	- když jsou dva se stejnou váhou - vyhraje ten zapsaný později (níže) v dokumentu
- **Dědičnost** 
	- element přebírá (dědí) vlastnosti od svého rodiče
	- pokud vlastnost není nadefinována (nebo není dědičná), tak použije výchozí vlastnost
	- ne všechny vlastnosti se dědí
		- **dědí se:** věci týkající se textu - barva, typ písma, velikost
		- **nedědí se:** věci týkající se rozvržení - rámečky, okraje, pozadí
- **Kaskáda** 
	- systém, který určuje, jaká hodnota bude nakonec použita
		- všechno vždy přebije **!important** (i inline styly)
		- hned po něm nastupuje **specifičnost (váha)** - vyšší váha přepíše ty nižší
		- **pořadí v kódu** - když 2 pravidla mají stejnou váhu a stylují stejný prvek, vyhraje to pravidlo, které je uvedeno níže v kódu
		- **výchozí styl prohlížeče**
## Specifičnost selektoru

| specifičnost | druh selektoru                        |
| ------------ | ------------------------------------- |
| 1000         | řádkový styl, přímo v html            |
| 0100         | identifikátor                         |
| 0010         | třída, pseudotřída, selektor atributu |
| 0001         | typový selektor, pseudoelement        |
| 0000         | univerzální selektor                  |

[[html - obrázky|předchozí]]