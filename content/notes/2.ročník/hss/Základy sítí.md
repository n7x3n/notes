---
date: 2026-10-06
author: n7x3n
---

# Modul 1 - sítě dnes
## Síťové komponenty
### Hostitelské role
- host - koncové zařízení (mobil, počítač, tablet), také nazýváni klienti
### Klient-server
- server je centrální prvek - všichni se připojují přes něj
- firmy, školy, jiné instituce
- různé druhy serverů např. Email server, web server, file server
### Peer-to-Peer
- bez centrálního prvku - tzv. decentralizovaná
- některé počítače mohou fungovat jako obojí - např. jako klient, ale také jako tiskárnový server
- **výhody:**
    - jednodušší
    - levnější
    - ideální pro jednodušší úkoly např. sdílení souborů nebo pro tiskárny
- **nevýhody:**
    - žádná centralizovaná administrace
    - není škálovatelná
    - počítače, které fungují i jako klient i jako server můžou být zpomalovány
### Koncové zařízení
- každé má vlastní adresu v rámci sítě
- je buď zdrojem nebo přijímačem dat vedené skrz síť
### Zprostředkující zařízení
- Router, switch, firewall...
- připojují jednotlivé koncové zařízení k síti
- mohou se připojit i na několik sítí
- používají adresu koncového zařízení společně s informacemi o síti k vybírání cesty skrz síť
### Síťová média
- proudí skrz ně komunikace od zdroje po příjemce

| jméno        | popis                                                           | hlavní výhoda | příklad užití                       |
| ------------ | --------------------------------------------------------------- | ------------- | ----------------------------------- |
| Copper (měď) | kroucená dvoulinka                                              | nejlevnější   | drátové připojení k místní síti     |
| Fiber-optic  | Skleněná vlákna; data cestují pomocí světla emitovaného laserem | nejrychlejší  | připojení sítí na velké vzdálenosti |
| Wireless     | Elektromagnetické vlnění na specifických frekvencích            | nejjednodušší | bezdrátové připojení k místní síti  |

---
## Reprezentace a Topologie
- umožňují zakreslování "mapy" sítí a zaznamenávání důležitých údajů o nich
- každá kategorie - [[#Koncové zařízení]] [[#Zprostředkující zařízení]] [[#Síťová média]] - má vlastní grafické znázornění
- terminologie navíc k zaznamenávání, jak jsou zařízení do sítě připojeny:
	- **Network Interface Card (NIC)** 
		- fyzicky připojují zařízení k síti
	- **Port** 
		- konektor nebo zásuvka na síťovém zařízení skrz který se médium připojuje ke koncovému nebo jinému síťovému zařízení
	- **Interface(Rozhraní)** 
		- specializované porty na síťovém zařízení které se připojují do individuálních sítí
		- porty na routeru jsou tedy nazývány *Network Interface*

- **Poznámka:** termíny Port a Interface jsou často zaměňovány
### Fyzické topologické diagramy
- zakreslují fyzické umístění všech zařízení
- ukazují, jaké zařízení je v jaké místnosti
### Logické topologické diagramy
- zakreslují zařízení, porty, a plán celé sítě
- ukazují, k čemu jsou jaké zařízení propojené, čím jsou data vedené a k jakému portu je co připojené
## Typy sítí
### LAN vs. WAN
#### LAN
- local area network - místní síť
- **typické znaky LAN:**
	- obsahuje zařízení umístěné ve fyzické blízkosti k sobě - ve škole, firmě, doma
	- většinou spravována jednou organizací nebo osobou
	- poskytují vysoko-rychlostní připojení pro zařízení v ní umístěné
#### WAN
- wide area network - rozsáhlá síť
- **typické znaky WAN:**
	- propojují LAN sítě přes rozsáhlé území - města, státy, kontinenty
	- spravovány několika různými organizacemi - často poskytovateli internetu
### Intranet vs. Extranet vs. Internet

#### Intranet
- soukromé připojení sítí LAN a WAN patřící společnosti
- přístupná pouze členy organizace, zaměstnanci nebo těmi s povolením
#### Extranet
- zabezpečený přístup lidem, kteří pracují pro jinou společnost ale potřebují přístup
- Příklad: nemocnice dá přístup doktorům, aby mohli sjednávat prohlídky pro své pacienty
#### Internet
- označení pro síť LAN a WAN sítí vzájemně propojených
- veřejně dostupný

![[intranet-extranet-internet.png]]

## Internetová připojení

### Domácí připojení

| Název     | popis                                                                                                               |
| --------- | ------------------------------------------------------------------------------------------------------------------- |
| Cable     | kabelovka; používá stejné kabely jako kabelová televize, rychlá, přístupná                                          |
| DSL       | rychlost, dobrý přístup, běží přes telefonní linky, může mít asymetrické rychlosti (download větší než upload)      |
| Cellular  | používají telefonní sítě (stejné jako mobilní data) k připojení k internetu; rychlost závisí na zařízení a vysílači |
| Satellite | Satelitové připojení; pomalejší; určené pro hůře dostupné lokace                                                    |
| Dial-up   | jakákoli telefonní linka; extrémně pomalé                                                                           |
| Fiber     | Optika; velmi rychlé se symetrickým downloadem a uploadem                                                           |

###  Připojení businessů
- oddělené od domácích připojeních
- často na vlastních linkách
- podobný výběr jako u domácích (stejné technologie, akorát na steroidech)
- větší důraz na stabilitu a rychlost
## Architektura sítí
- **čtyři základní charakteristiky sítí:**
	- **Fault Tolerance**
		- síť, která je schopná fungovat i při poruchách
		- spoléhají na vícero různých připojení v rámci sítě
	- **Rozšířitelnost**
		- možnost síť v jakýkoli moment rozšířit bez jejího dočasného limitování
	- **Quality of Service (Qos)**
		- regulace dat procházející skrz síť
		- např. prioritizování videohovorů oproti stahování souborů
	- **Zabezpečení**
		- Důvěrnost
		- Integrita
		- Dostupnost
## Nejnovější trendy
- hlavní aktuální trendy:
	- **Bring Your Own Device (BYOD)**
		- místo přiřazení firemního počítače si uživatel donese vlastní
		- správce sítě mu pak pouze udělí přístup
		- uživatelé mohou používat vlastní nástroje
	- **Online Collaboration**
		- spolupráce více lidí společně
	- **Video communications**
		- prostě videochat
	- **Cloud Computing**

#### Cloud Computing
- cloudové úložiště a aplikace



| Typ cloudu | popis                                                                                                                                  |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| Veřejný    | přístupné veřejnosti, zadarmo nebo pay-per-use, přístupné přes internet                                                                |
| Privátní   | přístupné pouze firmě nebo např. vládě, většinou na soukromé síti, s přísným zabezpečením přístupné i na dálku                         |
| Hybridní   | složený z dvou či více cloudů (např. částečně privátní, částečně veřejná), každá slouží jiným uživatelům, ale sdílí jednu architekturu |
| Komunitní  | podobné k veřejným, ale speciálně upravené pro potřeby organizace a zákony (např. HIPAA)                                               |
### Powerline sítě
- sítě používající elektrické kabely instalované ve zdích pro elektrickou síť k šíření signálu
- málo používané
### Wireless Broadband
- bezdrátové připojení k internetu v domácnostech viz [[#Domácí připojení|tabulka]] 

## Zabezpečení Sítě
- **běžné hrozby:**
	- **Virusy, worm a Trojské koně**
	- **Spyware a adware**
	- **Zero-day attack**
		- využívání bezpečnostních děr v software v den vydání
	- **Threat actor attack**
		- osoba napadne uživatelské nebo síťové zařízení
	- **Denial of service**
		- útok, který zpomaluje nebo crashuje aplikace
	- **Zachycování a krádež dat**
		- krádež dat ze sítě společnosti
	- **Krádež identity**
		- krádež přihlašovacích údajů a jejich zneužití na přístup k osobním datům
	
#### Řešení
- **základní řešení pro domácnosti:**
	- **Antivirus a antispyware**
		- aplikace na klientech
	- **Firewall filtrování**
		- nastavení softwarového firewallu na zařízení, aby filtroval co má a nemá přístup k počítači
- **řešení pro velké společnosti a organizace:**
	- **Dedikované firewall systémy**
		- více pokročilé
		- filtrují větší množství dat s lepší kontrolou
	- **Access control lists (ACL)**
		- dále filtrují přístup založené na IP adresách a aplikacích
	- **Intrusion prevention systems (IPS)**
		- identifikují rychle se šířící hrozby jako zero-day a zero-hour útoky
	- **Virtual private networks (VPN)**
		- zajišťují bezpečné připojení k organizaci na dálku