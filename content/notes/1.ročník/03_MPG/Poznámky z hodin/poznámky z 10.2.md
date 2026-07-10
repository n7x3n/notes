---
date: 2026-02-10
author: n7x3n
---
# zadání
- vytvoř program, kterému uživatel zadá 2 strany obdélníka
- program vypočítá jeho obvod a obsah
---
## 1. verze

```java 
import java.util.Scanner;
//Nejdřív musím otevřít scanner 
public class Main { 
	public static void main(String[] args) { 
		// musím si ten scanner vyvolat 
		Scanner sc = new Scanner(System.in);
		System.out.println("Zadáš 2 strany obdélníka. "); 
		/* zeptám se postupně na obě strany
		vždycky si je vložím do proměnné"int [jméno] = [jmeno-scanneru].nextInt ();*/ 
		System.out.println("Zadej 1. stranu: ");
		int a = sc.nextInt();
		System.out.println("Zadej 2. stranu: ");
		int b = sc.nextInt();
		/*spočítám si obvod a obsah 
	    samozřejmě odděleně*/
		int obvod = a+a+b+b;
		int obsah = a*b;
		// pak už jen vypíšu výsledek
		System.out.println("Obvod je " +obvod);
		System.out.println("Obsah je " +obsah);
		sc.close();
		}
} 
```

Poznámky ke kódu: 
- nepočítá se vložením nepoužitelného čísla do proměnných
- musím si vyvolat scanner pomocí <code>import java.util.Scanner;</code>
## 2. verze
(s kontrolou vložení správného čísla) 

```java 
import java.util.Scanner;
//Nejdřív musím otevřít scanner
public class Main {
	public static void main(String[] args) { 
		// musím si ten scanner vyvolat 
		Scanner sc = new Scanner(System.in); 
		System.out.println("Zadáš 2 strany obdélníka. "); 
		/* zeptám se postupně na obě strany
		vždycky si je vložím do proměnné "int [jméno] = [jmeno-scanneru].nextInt ();*/ 
		System.out.println("Zadej 1. stranu: "); 
		int a = sc.nextInt(); 
		System.out.println("Zadej 2. stranu: "); 
		int b = sc.nextInt(); 
		//spočítám si obvod a obsah, samozřejmě odděleně 
		int obvod = a+a+b+b; 
		int obsah = a*b;
		// tenhle prvek slouží k tomu, abychom vyřadili špatné nebo nevhodné hodnoty
		// první poznámkou if zjistím, jestli je první číslo větší, než 0 - tudíž vhodné
		// pokud je nevhodné první zadané číslo, vypíše to 
		if (a<= 0) { 
			System.out.println("První strana je špatně!");
		/*tento if slouží k zjištění, jestli druhé zadané číslo je vhodné
		pokud ne, vypíše to*/
		} else if ( b <= 0) { 
			System.out.println("Druhá strana je špatně.");
		// pokud jsou obě čísla vhodná - pouštím výsledky obvodu a obsahu 
		} else {
	    // pak už jen vypíšu výsledek 
			System.out.println("Obvod je " +obvod); 
			System.out.println("Obsah je " +obsah); 
		}
		sc.close();
	} 
} 
```

Poznámky: 
- stále by prošla negativní čísla

[[Data a datové struktury|předchozí]] [[poznámky z 12.2|následující]] 