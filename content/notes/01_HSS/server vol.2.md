---
date: 2026-05-22
---
# Hardwarové požadavky
## Základové desky
- víceprocesorové systémy
  - 2 až 8 patic pro CPU
- podpora ECC a Registered RAM
  - klíčové pro stabilitu
- Rozhraní
  - integrované SCSI/SAS řadiče a IPM/iDRAC pro vzdálenou správu
- Napájení
  - Připraveno pro redundantní záložní zdroje
## Procesory
- **Intel Xeon** a **AMD Epyc**
- **Hyper-Threading**
  - dvojnásobný počet vláken k počtu jader (když mám 4 jádra, tak máš 8 vláken)
- **Virtualizace**
  - HW podpora pro běh více OS na jednom fyzickém serveru 
## RAM
- **ECC**
  - (Error checking and correcting)
  - vyhledává a opravuje chyby v RAM v reálném čase
- **Registered RAM** 
  - obsahuje registr
  - hlídá komunikaci s čipsetem
- **Caching**
  - Místo extrémní rychlosti je priorita spolehlivost
## Úložiště a RAID
- disky se dávají do diskových polí aka RAID pro zvýšení rychlosti a spolehlivosti

[[Server|předchozí]]