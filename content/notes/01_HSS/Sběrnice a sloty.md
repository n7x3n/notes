---
date: 2025-10-25T14:01:00
---
# Sběrnice (ang. Bus)
- Součástí základní desky
- Svazek vodičů, kterými proudí data, řídící signály nebo adresy mezi komponenty počítače
- “centrální dálnice” mezi procesorem a okolí. Na rychlosti sběrnice hodně záleží.
- Přenos dat po sběrnici se řídí stanoveným protokolem
----
## Dělení
### Dělení dvou základních typů

1) Systémová
	- propojuje CPU a obvody na základní desce
2) Periferní(lokální)
	- spojuje CPU s okolními moduly (zakončena konektory – sloty)
### Sběrnici můžeme dělit dle typu přenášených dat
1) Datové (přenos dat)
2) Řídící (přenos řídících signálů od procesoru)
3) Adresní (přenos adres paměťových buněk
### Rozdělení podle způsobu přenosu dat
1) Sériová
	- data jsou přenášena pouze po jednom vodiči
	- velké přenosové rychlosti

2) Paralelní
	- data jsou přenášena současně po více vodičích
	- pracují na malé frekvenci

## Nejdůležitější parametry sběrnic
- Šířka přenosu - počet bitů, které lze zároveň po sběrnici přenést {bit}
- Frekvence - maximální frekvence, se kterou může sběrnice pracovat {Hz}
- Rychlost (propustnost) - počet bytů přenesených za jednotku času {B/s}
### Systémová sběrnice

- Spojuje procesor s nejbližším okolím (Ram, GPU, chipset – North bridge a ostatní obvody desky)
- Umístěná na základní desce
- Přes patici spojena procesorem
- Sběrnice je součástí desky konstrukce závislá na výrobci -> nutná kompatibilita s chipsety (jiný výrobce)
- Dva základní modely
	1) intel se sběrnicí FSB
	2) AMD se sběrnicí HyperTransport (integrovaný paměťový řadič)

## Typy systémových sběrnic

1. Front Side Bus (FSB) propojuje CPU s hlavní pamětí a dalšími klíčovými komponenty na základní desce. FSB hraje klíčovou roli při stanovení celkové rychlosti a účinnosti počítačového systému
2. Back side bus (BSB) propojuje CPU s mezipamětí (cache), umožňuje rychlejší přenos dat mezi CPU a mezipamětí, čímž zvyšuje celkový výkon systému
3. Paměťová sběrnice je druh sběrnice, která propojuje CPU s pamětí systému, umožňuje výměnu dat mezi nimi; její rychlost a šířka ovlivňují paměťovou propustnost systému
4. Peripheral component interconnect express (PCIe) sběrnice umožňuje komunikaci mezi CPU a periferními zařízeními, jako jsou grafické karty, síťové karty a řadiče úložišť, klíčová pro rozšíření systému.
---
# Konektory
## Interní konektory

- IDE starší typ konektoru pro připojení pevného disku nebo optické mechaniky
- SATA - modernější typ konektoru plnící stejnou funkcí jako předchozí IDE
- Floppy/FDD - dnes již téměř nepoužívaný port pro připojení disketové mechaniky
- USB a Firewire - umožňující vyvést tyto typy portů na zadní nebo přední stranu počítače; to se hodí tehdy, když chcete k počítači připojit třeba USB disk; nemusíte tak hledat konektor vzadu
- Konektor ventilátorů - slouží k zapojení přídavných větráků a chladičů
- Konektory zvukové karty
## Externí konektory

- USB- nejrozšířenější počítačové rozhraní pro připojení všech moderních periferních zařízení
- Ps/2 - starší konektor pro myši a klávesnice
- Firewire - rychlé rozhraní pro připojení digitálních kamer a případně externích pevných disků
- COM/LPT - dvojice portů, které dnes již nemají hlubší použití - plně je vytlačilo USB; dříve se do nich zapojovala myš, tiskárna nebo modem
- D-Sub, DVI, HDMI, DisplayPort - analogový (D-Sub), popř. Digitální výstupy z grafické karty pro připojení monitoru
- LAN (RJ-45) - slouží pro připojení síťového kabelu standardu UTP
- 3,5 mm jack- bývají běžně zastoupeny ve třech nebo šesti výstupech a slouží k zapojení patřičné audio soustavy a mikrofonu
- S/PDIF - digitální konektor pro připojení reproduktorů, koaxiální nebo optická
----
# Konktrétní sběrnice
## AGP (accelerated Graphics port)
- určena pro přenos dat do zobrazovací soustavy
- paralelní sběrnice
- šířka 32 bitů
- nahrazena sběrnicí PCI Express
- propojuje grafický adaptér přímo s North Bridge
- Standardy 1x,2x,4x,8x
## PCI (peripheral component interconnect
- Pci-X (extended)
- Především pro pentia
- Paralelní sběrnice
- Dnes nahrazována PCI Express
- Novinka pro instalaci rozšiřujících desek – plug and play
- 32 a 64 bitové sloty
- Sloty opatřeny zámky
- V roce 2003 pci – X 2.0 až 533MHz s šířkou sběrnice 4,3 GB/s

## PCIe 
- Nahrazuje PCI a AGP
- Sériová sběrnice
- OS a HW nemá již problémy při spolupráci se sběrnicí, podporuje hot plug and hot swap
- Standardy:PCie 1x, 4x, 8x, 16x
- Rok vzniku 2003
- Dnes se považuje za standard
- Univerzální vstupní-výstupní sběrnice
- 6 verzí PCI-e 1.0 až PCI-e 6.0

## SCSI (small computer system interface)
- Rozhraní, které bylo používáno k připjení např. Harddisků, scannerů, tiskáren nebo mechaniky
- Založené na starší sběrnici

## IDE/ATA
- Western digital, 1986
- Paralelní sběrnice pro připojování zařízení k zachování dat
- Rozhraní ata prošlo dlouhým vývojem kde na začátku se nazývalo IDE, pozdeji také EIDE UATA
- Po příchodu SATA se přejmenovalo na PATA
- Na jednu ATA – 2 zařízení; master a slave (tzv.kšandy)
- Rychlosti 3,3MB/s až po 22MB/s
- IDE=ATA=PATA
## SATA
- Sériová sběrnice pro připojení velkokapacitních paměťových zařízení
- Dnešní standard
- Vyvinuta v 2000 firmou Serial ATA working group
- Tenčí kabely a vyšší rychlosti  
- 1.verze 1.5Gbit/s 
- Dnes verze 3: 6/Gbit/s (750MB/s) 
- Převážně pro HDD, SSD 
- Podporuje hot swapping 
- eSATA- externí verze SATA, pro připojování externích zařízení 
- Pro notebooky také verze mSATA
## IEEE 1394/Firewire 
- Vysokorychlostní sériová sběrnice, Apple 
- Slouží k připojení externích disků, tiskáren, kamer, scannerů, a jiných periferií 
- Sony- pod názvem i.LINK 
- Samotné standardy IEEE byly zavedeny v roce 1995, i když design začal již v roce 1986 
- Plug&Play a Hot-swapping 
## USB (universal serial Bus) 
- Nejrozšířenějším slotem pro připojení (v podstatě) čehokoliv 
- V současnosti nejvíce používaná USB 2.0, 3.2 Gen 1 
- Plug&play 
- Propojení na vzdálenosti až 5m 
- Možnost napájení z konektoru 
- Type-A, Type-B, microUSB, USB-C 
## M.2 
- moderní rozhraní pro připojení rozšiřujících karet – SSD, Wi-Fi moduly, zvukové karty 
- Vysokorychlostní přenos dat 
- klíče na M.2 slouží k zajištění správného zapojení karty do slotu a a určují typ rozhraní, nejběžnější klíče jsou B a M 
Klíč B: podporuje PCIe x2, SATA, USB 2.0, USB 3.0, audio, UIM, HSIC a SATA rozhraní
Klíč M:PCIwex4 SATA, vyšší rychlost, než klíč B 

## Rozhraní COM 
- Patřil mezi nejpoužívanější počítačový port 
- Sériový port

## Rozhraní LPT 
- Paralelní port 
- Zastaralý 
- Používaný pro tiskárny

[[Základová deska|předchozí]] [[Procesor|následující]] 