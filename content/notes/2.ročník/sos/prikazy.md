---
date: 2026-10-09
author: n7x3n
---

## uživatelé


| příkaz                                               | funkce                                              |
| ------------------------------------------------------| -----------------------------------------------------|
| net user                                             | výpis aktivních účtů                                |
| net user jmeno                                     | konkrétní info o jedno účtu                         |
| net user jmeno heslo                            | změna hesla pro účet                                |
| net user jmeno /active:no                          | deaktivace účtu                                     |
| net user jmeno /active:yes                         | aktivace účtu                                       |
| net user jmeno /passwordchg:no                     | zakázání změny hesla                                |
| net user jmeno heslo /add /fullname:"celé jméno" | vytvoření uživatele s heslem s plným jménem         |
| net user jmeno heslo /add /fullname:"celé jméno" | vytvoření uživatele s proptem na nastavení hesla    |
| net user jmeno /times:Po-Pá,6-16                   | přístup k účtu pouze od Pondělí do Pátku od 6 do 16 |
| net user jmeno /delete                             | smazání účtu                                        |
| net user jmeno /times: all | povolení na dobu |


## skupiny

| příkaz | funkce | 
| --- | --- | 
| net localgroup | výpis skupin |
| net localgroup jmeno | výpis konkrétní skupiny |
| net localgroup jmeno-skupiny /add | vytvoření skupiny |
| net localgroup jmeno-skupiny uzivatel /add | přidání člena do skupiny |
| net localgroup jmeno-skupiny uzivatel /add | odebrání člena ze skupiny |
| net localgroup jmeno-skupiny /delete | smazání skupiny |

