---
date: 2026-03-24
author: n7x3n
---
# podmínky
## do while (podmínka)
- spustí se a po prvním cyklu zjistí, jestli podmínka platí

## while (podmínka) do
- než se spustí, zjistí, jestli podmínka platí a až potom se spouští
---

# hádání čísel
## první verze
- bez randomizace čísla
- bez počítání pokusů
```java
/*
Naprogramuj hru. Program si bude myslet číslo 1-100. Užvatel bude hádat. Odpovědi: přidej/uber/trefa
*/
//import scanneru
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    //otevřu si scanner
	    Scanner sc = new Scanner(System.in);
	    //do proměnné si (prozatím) vložím číslo
	    int tajemnecislo = 69;
	    //udělám si proměnnou tip
	    int tip;
	    //vypíšu uživateli, ať hádá
		System.out.println("Myslím si číslo. Zkus ho uhodnout");
		do {
		    //uživatelův tip vložím do proměnné tip
		    tip = sc.nextInt ();
		    //pokud je tip menší, než tajemnecislo, tak vypíše přidej
		    if (tip < tajemnecislo) {
		        System.out.println("Přidej");
		        //a když je tip větší, tak vypíše uber
		    } else if (tip > tajemnecislo) {
		        System.out.println("uber");
		        //když se trefím, vypíše zásah
		    } else {
		        System.out.println("zásah!");
		    }
		    //nastavím, ať se tento cyklus opakuje, dokud se tip nerovná tajemnecislo
	    } while (tip != tajemnecislo);
	}
}
```
---

## druhá verze
- funkční randomizace
- funkční počitadlo pokusů
```java
/*
Naprogramuj hru. Program si bude myslet číslo 1-100. Užvatel bude hádat. Odpovědi: přidej/uber/trefa
*/
//import scanneru
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    //otevřu si scanner
	    Scanner sc = new Scanner(System.in);
	    int tajemnecislo = (int) (Math.random() * 100 + 1);
	    //udělám si proměnnou tip
	    int tip;
	    //udělám si proměnnou na počet pokusů
	    int pocetpokusu = 0;
	    //vypíšu uživateli, ať hádá
		System.out.println("Myslím si číslo. Zkus ho uhodnout");
		do {
		    //uživatelův tip vložím do proměnné tip
		    tip = sc.nextInt ();
		    //při každém cyklu přičtu 1 do proměnné pocetpokusu
		    pocetpokusu++;
		    //pokud je tip menší, než tajemnecislo, tak vypíše přidej
		    if (tip < tajemnecislo) {
		        System.out.println("Přidej");
		        //a když je tip větší, tak vypíše uber
		    } else if (tip > tajemnecislo) {
		        System.out.println("uber");
		        //když se trefím, vypíše zásah
		    } else {
		        System.out.println("zásah!");
		    }
		    //nastavím, ať se tento cyklus opakuje, dokud se tip nerovná tajemnecislo
	    } while (tip != tajemnecislo);
	    System.out.println("Zvládl jsi to na "+pocetpokusu+". pokus");
        sc.close();
	}
}
```


[[poznámky z 17.3|předchozí]] [[poznámky z 31.3|následující]]