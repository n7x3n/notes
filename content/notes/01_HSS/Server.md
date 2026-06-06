---
date: 2026-05-15
---

# Servery
- prostě komp v nepřetržitém provozu =)
## Architektury
### klient-server
- server jako centrální prvek
- veškerá komunikace jde přes něj
### peer-to-peer
- žádný centrální prvek
- každý se připojuje ke každému
- decentralizovaná správa
---
#### torrentové okénko
- **Leech** - stahuje
- **Seed** - poskytuje soubor -> od něho se stahují soubory
- **Peers** - seedeři + leeches
---

## princip komunikace
- **daemon** 
  - program na serveru
  - neustále očekává výzvy klientů
- **Protokol**
  - scénář komunikace stanovující pravidla a pořadí otázek a odpovědí

### porty
| Port  | Protokol             | Význam                       |
| ----- | -------------------- | ---------------------------- |
| 20,21 | FTP                  | přenos souborů mezi pc       |
| 22    | SSH (secure shell)   | vzdálený šifrovaný přístup   |
| 25    | SMTP (mail transfer) | Odesílání elektronické pošty |
| 80    | HTTP                 | služba WWW - webové stránky  |
| 443   | HTTPS                | webové stránky s šifrováním  |
| 110   | POP3                 | vzdálený přístup do schránky |

- SMTP a POP3 jsou k mailu <- nutno vědět
## Provedení hardwaru
- **Tower**
  - klasická skříň
- **Blade**
  - moduly propojené sběrnicí v kontejneru
- **Rack**
  - standardizované moduly montované do ocelového rámu
  - to, co si každý představí pod pojmem "server"
### Racková jednotka (U)
- rack = ocelový rám, do kterého se umisťují servery do sloupce nad sebe
- 1U = 1,75 palce
- U - rack Unit
---
## Typy serverů dle služeb
#### Webový
- Hosting stránek (html, php)
#### Tiskový
- Sdílení tiskárny po síti
#### Databázový
- Strukturovaná úložiště dat
#### Proxy
- Prostředník mezi klientem a cílem
#### Souborový
- Centrální datové úložiště
#### Herní
- Poskytuje výkon pro multiplayer
---
## DNS
- Domain name system
- k webovkám se připojujeme pomocí ip adres a čísla portu (např. 192.168.145.32:5050)
- DNS přiřadí k této ip adrese doménové jméno (např. youtube.com)

[[Periferie vol.2|předchozí]] [[server vol.2|následující]]