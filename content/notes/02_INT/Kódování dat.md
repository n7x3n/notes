---
date: 2025-10-22T15:50:00
author: n7x3n
---
- Kódování dat je proces, při kterém se informace převádí do určité podoby (kódu), aby je bylo možné jednoznačně uložit, přenášet nebo zpracovávat počítačem.
## Další pojmy

##### **Kódování**
převod informací do podoby dat (např. písmeno „A“ → 01000001). 
##### **Šifrování**
utajení obsahu dat. 
##### **Komprese**
zmenšení objemu dat
## Ukázky mimo počítače
- Morseova abeceda 
převod písmen na tečky a čárky. 
##### **Braillovo písmo** 
převod písmen na reliéfní body. 
##### **Vlajkový kód**
převod na polohy vlajek.
## Kódování znaků a čísel v počítači
### Znakové kódy
- ASCII tabulka (7 bitů ⇒ 128 znaků) 
- Rozšíření (ISO 8859-2) - čeština 
- Unicode / UTF - 8 dnešní standard
### Čísla
- Celá čísla (binární zápis)
- Reálná čísla (s plovoucí desetinnou čárkou, problém při zápisu a někdy i počítání)

## Multimedia
- obrázek, zvuk i video musí být převedeny do číselné podoby
- Problémy: velký objem dat -> nutnost komprese
- Cíl: co nejvěrnější uchování informace při co nejmenší velikosti souboru
### Bitmapové obrázky (rastry)
- Ukládají každý pixel jako kombinaci barev (např. RGB).
- Velký soubor: obrázek 1920×1080 pixelů, 3 bajty na pixel → cca 6 MB.
- Formáty:
	- BMP – bez komprese, obrovské soubory.
	- PNG – bezztrátová komprese, vhodné pro grafiku, loga.
	- JPEG (JPG) – ztrátová komprese, vhodné pro fotografie (malé soubory).
### Video
- Video = **sekvence obrázků + zvuková stopa**.
- Velmi náročné na objem dat → nutná  
komprese.
- Formáty:
	- AVI – starší formát, slabší komprese.
	- MP4 (H.264, H.265) – moderní, účinná komprese, menší velikost.
	- MKV – kontejner, může obsahovat více stop (video, zvuk, titulky).
### Zvuk
- Zvuk je analogový → vzorkování (digitalizace).
- **Vzorkovací frekvence** (např. 44,1 kHz pro CD).
- **Bitová hloubka** (např. 16 bitů na vzorek).
- Formáty:
	- WAV – nekomprimovaný zvuk, velké soubory, ale kvalitní.
	- MP3 – ztrátová komprese (odstraní tóny, které člověk neslyší).
	- FLAC – bezztrátová komprese (menší než WAV, kvalita zachována).
**Vzorkování**
![[Pasted image 20251023224650.png]] 
**Kvantování (bitová hloubka)**
![[Pasted image 20251023224729.png]]
**Digitální signál**
![[Pasted image 20251023224746.png]]
[[Model]] 