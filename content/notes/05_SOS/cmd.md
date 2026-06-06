---
date: 2026-04-28
title: Příkazový řádek
---
# Základy příkazového řádku
- co je v závorkách -> přepiš podle potřeby
## Základní příkazy
| příkaz     | použití                                            |
| ---------- | -------------------------------------------------- |
| help       | nápověda                                           |
| cls        | vyčištění obrazovky                                |
| tree       | ukáže strukturu složek                             |
| color      | změna barvy pozadí XY -> X = pozadí, Y = text      |
| date       | vypíše datum popř. ho změní                        |
| time       | vypíše čas popř. ho změní                          |
| systeminfo | vypíše info o pc                                   |
| start      | spustí programy, soubory nebo otevře nové okno cmd |

---
## Práce se složkami

| příkaz                     | použití                              |
| ----------------------------| --------------------------------------|
| dir                        | vypíše obsah složky                  |
| cd (cesta)                 | změna složky                         |
| mkdir (název)              | vytvoření složky                     |
| rmdir (název)              | odstranění prázdné složky            |
| rmdir /s /q                | odstranění složky včetně obsahu      |
| ren (staré jm.) (nové jm.) | přejmenování složky                  |
| move (zdroj) (cíl)         | přesun                               |
| xcopy (zdroj) (cíl)        | kopírování složky, bacha na atributy |

---
## Práce se soubory

| příkaz                         | použití                                         |
| ------------------------------ | ----------------------------------------------- |
| type nul > (název )            | vytvoření prázdného souboru                     |
| echo (text) > (název)          | vytvoření souboru a vpis textu do něj           |
| robocopy (zdroj) (cíl) /MIR    | robustní kopírování (zrcadlení)                 |
| ren (starý název) (nový název) | přejmenování souboru                            |
| type (název)                   | zobrazí obsah souboru                           |
| del (soubor)                   | smazání souboru                                 |
| del /f /q *.log                | tiché smazání více souborů                      |
| dir (název)                    | hledá soubory, /s pro hledání i v podadresářích |
| dir *.log                      | hledá pouze soubory s příponou log              |

[[Windows|předchozí]]