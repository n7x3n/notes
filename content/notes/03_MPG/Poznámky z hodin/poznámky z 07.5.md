---
date: 2026-05-07
---

# Opakování

## podmínka for

```java title="hvěždičkovač"
/*
Uživatel zadá, kolik chce hvězdiček a program mu je na řádku vypíše.
Na dalším řádku se program rozloučí.
*/
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    Scanner sc = new Scanner(System.in);
		System.out.println("Kolik chceš hvězdiček? ");
		int hvezda = sc.nextInt();
		// kontroluje počet řádků s hvězdičkama
		for (int i=1; i<= hvezda ;i++) {
		    /* vypisuje hvězdičky na řádky
		    vezme j a dá do něj 1
		    dokud vypíše míň hvězd než číslo řádku, tak vypisuje dál */
		    for (int j = 1;j<=i ;j++ ) {
		        System.out.print("*");
		    }
		    System.out.println();
		}
		// \n -> newline -> vypíše text na další řádek
		System.out.println("\nhotovo");
	}
}
```

---

```java title="hádač"
/*
Uživatel zadá číslo. Pokud bude 0, program končí. 
Pokud bude něco jiného, ta se program znovu zeptá na číslo...
*/
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    Scanner sc = new Scanner(System.in);
		int cislo;
		do {
		    System.out.println("zadej číslo");
		    cislo = sc.nextInt();
		} while (cislo != 0);
		System.out.println("Konec");
		
	}
}
```

---

```java title="fancy počitadlo"
/*
program se zeptá na 7 čísel, ke kterým potom:
- vypočítá průměr
- sečte počet kladných zadaných čísel
- určí největší a nejmenší číslo
*/
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    Scanner sc = new Scanner(System.in);
	    double cislo;
	    double min = Double.MAX_VALUE;
	    double max = Double.MIN_VALUE;
	    double soucet = 0;
	    int pocetKladnych = 0;
	    
	    for (int i = 1; i <=7 ; i++) {
	        System.out.println("Zadej "+i+".číslo");
	        cislo = sc.nextDouble();
	        soucet += cislo;
	        if (cislo > max) {
	            max = cislo;
	        } 
	        if (cislo < min) {
	            min = cislo;
	        }
	        if (cislo > 0) pocetKladnych++;
	    }
	    System.out.println("nejmenší je: "+min);
	    System.out.println("největší je: "+max);
	    System.out.println("Průměr je "+(soucet/7));
	    System.out.println("Počet kladných je "+pocetKladnych);
	    }
}
```



[[poznámky z 05.5|předchozí]] 