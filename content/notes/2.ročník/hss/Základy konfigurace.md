---
date: 2026-11-02
author: n7x3n
---

# Návod (tak trochu)

## Konfigurace switche

### Základní připojení
1. Propoj si počítač se switchem
2. otevři si terminál na počítači
3. dostaň se do privilegovaného režimu - ``enable``

### Základní konfigurace
1. vstoupit do konfiguračního režimu - ``configure terminal``
    - terminál by ti měl psát něco jako ``switch(config)#``
2. nastav jméno switche - ``hostname meno``
3. nastav banner - ``banner motd #zprava pro banner#``
4. nastav si pro privilegovaný režim heslo - ``enable secret heslo``

### Konfigurace linky
1. přejdi do režimu pro konfiguraci konzole - ``line console 0``
    - terminál by ti měl teď psát ``switch(config-line)#``
2. nastav pro ni heslo - ``password heslo``
3. aktivuj heslo - ``login``
4. vycouvej do configu - ``exit``
5. přejdi do configu pro vty - ``line vty 0 15``
6. zase heslo - ``password heslo``
7. zase aktivuj - ``login``
8. vycouvej - ``exit``
    - terminál by měl psát ``switch(config)#``

### Konfigurace Vlanu
1. přejdi do režimu konfigurace interface vlanu - ``interface Vlan1``
2. nastav ip adresu a masku
    - příkaz ``ip address`` chce 2 parametry- > ip adresu a masku
    - např. ``ip address 192.168.10.15 255.255.255.0``
    - potom příkaz ``no shutdown``
3. bež zpátky do configu pomocí ``exit``
    - terminál píše ``switch(config)#``
- **Pro jistotu:** gateway se nastavuje pomocí ``ip default-gateway`` a ip adresy
    - např. ``ip default-gateway 192.168.10.25``

### poslední kroky
1. v ``switch(config)#`` enkryptuj hesla - ``service password-encryption``
2. vycouvej pomocí ``exit`` do globálního režimu ``switch#``
    - můžeš si zkontrolovat konfiguraci pomocí ``show running-config``
3. ulož si konfiguraci - **Zavrč si** - ``wr``

---

## Konfigurace počítače
1. otevři si ip configuration na počítači
2. přepni na static a vyplň ip adresu a masku
3. hotovo =)

## Ověření na počítači
1. propoj si počítač síťovým kabelem
2. otevři command prompt
3. pošli packet na ip adresu ``ping 192.168.10.15``