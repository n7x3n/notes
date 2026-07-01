---
date: 2026-01-27
author: n7x3n
---
# Odkazy
- V textu jsou vizuálně odlišeny - modrý, podtržený
- 3 části
	1. Umístění
	2. Název - vidí uživatelé, text nebo obrázek
	3. Cíl - nová karta nebo okno; často dělá prohlížeč
## URL - adresa souboru
- (Uniform Resource Locator)
- přesná specifikace umístění zdrojů
- URL = internetová adresa
## Typy odkazů
### 1. Hypertextový odkaz
- element  <<code>a</code>>
```html
<a href="stranka.html">Název odkazu</a>
```

- <code>href</code> - adresa/cesta souboru
- dělí se na:
#### Absolutní odkaz
- používá se pro odkazování na dokument umístěný na jiném serveru - např. na jinou webovku
```html
<a href=“http://www.oaveseli.cz/stranka.html“>Název odkazu</a>
```

#### Relativní odkaz
- používá se při odkazování na stránky v rámci naší stránky
- prohlížeč sám doplňuje URL
- pokud se nachází odkazovaný soubor ve stejném adresáři - stačí napsat jenom jméno souboru
```html
<a href="uvod.html">Úvod</a>
```

**Pokud se nachází v jiném adresáři:**
```html
<a href="referaty/cestina/obrozeni.html">Národní obrození</a>
```

- ==pokud je v adresářové struktuře výš, použijeme dvě tečky( např. ". ./images/fotka.jpg)==
##### Pozor!!! (blokové odkazy)
```html
<a href="utek-zirafy.html">
  <hgroup>
    <h1>Žirafa utekla ze zoo</h1>
    <h2>Zvířata po celém světě se radují</h2>
  </hgroup>
</a>
```

### 2. Jmenný odkaz (kotva)
- přenesení do specifické části stránky
- funguje i v kombinaci s přenesením z jiné stránky
- ==odkazované místo== - atribut ==name nebo id==
- příklad označení u nadpisu:
```html
<h2 id="kap6">Kapitola 6</h2>
```
- odkazování stejné, jako u hypertextového odkazu, pouze doplněné o # (hashtag)
- vypisujeme hodnotu z <code>id</code>
```html
<a href="#kap6"> Kapitola 6</a>
```
- pokud je jmenný odkaz na jiné stránce, nebo serveru - potřeba zadat celou cestu
>[!TIP] tip
>- název odkazu by neměl být příliš dlouhý
>- nepoužijeme výrazy "klepněte sem"
>- název odkazu lze stylovat v CSS

### 3. Jiné typy odkazů
- odkazy na:
	1. na soubor
	2. na e-mail
	3. na stránky FTP
#### Odkaz na soubor
- "slušné" upozornit na velikost souboru, nejlépe do závorky
```html
<a href=“soubory/navod.pdf“>Návod k obsluze</a>
```
#### Odkaz na e-mail
- použití "mailto" - za ním e-mailová adresa
- otevře okno s e-mailovým klientem
- je dobré mail i jako název (když někdo nemá mailového klienta)
```html
<a href=“mailto:skola@oaveseli.cz“>skola@oaveseli.cz</a>
```
#### Odkaz na stránky FTP
```html
<a href=“ftp://ftp.stranky.cz“>FTP stránky </a>
```
## Formátování odkazů
- pomocí CSS
- nebo pseudo-elementů
### Odkaz s obrázkem
```html
<a href=“stranka.html“><img
src=“../images/geometry/triangle_red.png“></a>
```
### Odkaz v novém okně
```html
<a href="http://www.oaveseli.cz" target="_blank">OA Veselí n. M.</a>
```
### Titulek odkazu
- má přiblížit, kam odkaz směřuje
- ==atribut title==

[[Formátování textu|předchozí]]  [[html - obrázky|následující]]
