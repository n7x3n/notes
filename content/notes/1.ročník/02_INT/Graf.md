---
date: 2025-10-23T23:04:00
author: n7x3n
---
## Co je to graf?
- model reality, který popisuje objekty a jejich vzájemné vztahy pomocí bodů a spojnic
- nepředstavuje skutečnou hodnotu, ale zjednodušený obraz
- zaměřuje se jen na to, jak jsou prvky propojené
## Struktura grafu
- **Vrcholy (uzly)** – reprezentují **objekty nebo prvky systému** (např. města, osoby, počítače, úkoly).
- **Hrany (spojnice)** – znázorňují **vztahy nebo vazby**  mezi těmito objekty (např. cesty, přátelství, kabely, závislosti).
- Někdy hrany mohou mít i **vlastnosti** – např. **směr**, **váhu** (vzdálenost, čas, cena) nebo **typ vztahu**.
### Neorientovaný graf
- **Hrany nemají směr** — spojují vrcholy oboustranně.
- Zapisují se jako **neuspořádané dvojice** {A, B}.
- Používá se tam, kde směr **není důležitý**
- např.  silniční mapa obousměrných cest, vztahy mezi lidmi, sítě počítačů.
- **Příklad:** Vrchol A je spojen s B → lze jít z A do B i z B  
do A.
### Orientovaný graf (digraf)
- **Hrany mají směr** — ukazují „odkud → kam“.
- Zapisují se jako **uspořádané dvojice** (A, B).
- Používá se tam, kde směr **hraje roli** 
- např.  jednosměrné silnice, tok informací, e-mail, závislosti úkolů, datové toky.
- **Příklad:** Z uzlu A vede šipka do uzlu B → můžeme jít z A do B, ale ne naopak.
## K čemu se grafy používají v modelování
Grafy umožňují:

- přehledně **znázornit složité vztahy** mezi prvky systému,
- **analyzovat strukturu** 
	- (např. kdo je propojen s kým, kudy vede nejkratší cesta),
- **hledat řešení problémů** – trasy, závislosti, optimalizace.