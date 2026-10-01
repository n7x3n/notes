---
date: 2026-09-24
author: n7x3n
---

# Metoda
## Proč se metody používají
- zkracují kód (napíšu jednou, použiju víckrát)
- zlepšují čitelnost (názvy metod většinou shrňují, co metoda dělá)

## Jak se zapisují
- zapisuje se malým počátečním písmenem
- za názvem závorka
-  píše se ve formátu ``verejnost trida navratovy-typ jmeno(parametry){kód}``

```java
public static void main(){}
```

## veřejnost

- kdo ji může používat
  - **public** - kdokoli v projektu mohou používat
  - **...** (nenapíšu nic) - všichni v balíčku(podadresáři) mohou používat
  - **protected**
  - **private** - to může používat jenom jeden určitý (použiju, když mám objekt a nechci, aby mi do něj někdo lezl)

## třida
- **static** - může ji používat celá třída
- **...** (nenapíšu nic)  - tzv. **Instanční** - může ji používat celá instance, celý objekt

## Návratový typ
- **void** = procedura
  - vykonej a skonči
  - bez ``return``u

- **s návartovým typem**
  - je tam datový typ (int, double, String...)
  - musí být ``return``
## parametry
  - buď tam nic není
  - nebo jsou tam zadané proměnné(např. ``int number``)
  - vstupy se berou postupně

---

```java title="VypocetCtvercu"
import java.util.Scanner;

public class VypocetCtvercu {
    static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        pozdrav();
        int strana = sc.nextInt();
        System.out.println("Obvod čtverce je " + obvod(strana));
        System.out.println("Obvod čtverce je "+obsah(strana));
    }

    static void pozdrav(){
        System.out.println("Ahoj, já jsem program na výpočet čtverců.");
        System.out.println("Zadej stranu čtverce");
    }
    static int obvod(int a){
        return 4*(a);
    }
    static int obsah(int a){
        return (a)*(a);
    }
}
```