---
date: 2026-03-10
---
# Cyklus pomocí for
- cyklus u kterého dopředu vím, kolikrát se provede
- skládá se (v podstatě) ze tří částí
```java
for (inicializace; podmínka; aktualizace) {
}
```
- **inicializace:** obsahuje proměnnou (většinou i) proběhne jen jednou a nastaví úvodní hodnotu proměnné
- **podmínka:** v podstatě <code>if</code> - před každým opakováním se na ni program zeptá a pokud je odpověď<code>true</code>, tak se kód provede
- **aktualizace:** tady se změní hodnota proměnné z inicializace (např. přičítání 1), aby cyklus mohl skončit
# hvězdičkový program
```java
/*Uživatel zadá číslo a program vypíše tolik * každou hvězdičku dá na nový řádek a ke každé hvězdičce přidá pořadové číslo např. "1. *" */ 
//importuju si scanner 
import java.util.Scanner;
public class Main 
{
	public static void main(String[] args) { 
		//otevřu si scanner
		Scanner sc = new Scanner(System.in);
		//zeptám se na číslo
		System.out.println("zadej číslo");
		int cislo = sc.nextInt ();
		/*for je pro opakování 
		vezme to i, které je jedna 
		dokud bude i < zadané číslo, tak bude dopisovat hvězdičky*/
	 for (int i = 1; i <= cislo; i++) {
		//program vždy vypíše pořadové číslo - proměnnou i a pak vypíše hvězdičku
		 System.out.println(i+". *"); 
		 } 
		 /*vypíšu končím
		 to \n je pro odřádkování*/
		 System.out.println("\nkončím");
		 //zavřu scanner
		 sc.close();
	}
}
```


[[poznámky z 12.2|předchozí]] [[poznámky z 17.3|následující]]