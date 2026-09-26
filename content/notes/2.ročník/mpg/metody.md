---
date: 2026-09-24
author: n7x3n
---

# Metoda

- zapisuje se malým počátečním písmenem
- za názvem závorka

```java
public static void main(){}
```

## veřejnost

- kdo ji může používat
  - **public** - kdokoli v projektu mohou používat
  - **...** (nenapíšu nic) - všichni v balíčku(podadresáři) mohou používat
  - **protected**
  - **private** - to může používat jenom jeden určitý (použiju, když mám objekt a nechci, aby mi do něj někdo lezl)

## metoda třídy
- se slovem **static** ji může používat celá třída
- bez něj ji může používat celá třída

## Návratový typ
- **void** = procedura
  - udělej a skonči
  - bez ``return``u

- **s návartovým typem**
  - je tam datový typ (int, double, String...)
  - musí být ``return``
- **parametrická**
  - buď tam nic není
  - nebo je tam něco zadané
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