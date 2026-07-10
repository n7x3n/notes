---
date: 2026-03-31
author: n7x3n
---
# první program
```java
/*
Uživatel zadá celé číslo. Zjistěte a vypište
- jestli je to číslo větší než 0
- jestli je sudé
- vypočítej číslo na druhou + číslo děleno 2
- vypiš tolik písmen "C" kolik je to číslo velké
- když je to číslo menší než nula nebo nula, napiš "error"
*/
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    Scanner sc = new Scanner(System.in);
		System.out.println("Napiš číslo ");
		int cislo = sc.nextInt();
        //když číslo není nula a je větší než nula
		if (cislo != 0 && cislo >= 0){
            System.out.println("Číslo je kladné a není nula");
            //jinak:		    
		} else {
		    System.out.println("Číslo je záporné, nebo nula");
		}
		if (cislo % 2 == 0) {
		    System.out.println("Číslo je sudé");
		} else {
		    System.out.println("Číslo je liché");
		}
		double vysledek = (cislo*cislo+cislo)/2;
		System.out.println("Výsledek je "+vysledek);
		for (int i = 1;i<=cislo ;i++ )
		System.out.println(i+". c");
	}
}
```
- nemám tam tu část s tím errorem


```java
cislo % 2 == 0
```
- pro zjištění, jestli je číslo sudé
- to <code>%</code> znamená -> zbytek po dělení
- celý ten výraz znamená: " když vezmu číslo a vydělím ho dvěma, tak zbytek má být 0

```java
double vysledek = (cislo*cislo+cislo)/2.0;
```
### Když chci aby tohle bylo na desetinné
- **double** - aby byla proměnná s desetinným
- **2.0** - tohle donutí javu, aby dělila na desetinné (nevím proč =))

**Tabulka s početními operátory:** [[Početní operátory v javě|zde]] 

[[poznámky z 24.3|předchozí]] [[poznámky z 16.4|následující]] 