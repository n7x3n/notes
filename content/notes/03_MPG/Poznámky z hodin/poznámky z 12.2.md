---
date: 2026-02-12
---
# Podmínky
## a - AND 
- zápis -  <code>&&</code> 
- Vždycky musí platit všechny podmínky - pokud mám 2 výroky (výrok A a B) musí platit oba 
- Logický součin 
##  nebo - OR
- zápis - <code>||</code> 
- Stačí, aby platil jenom jeden výrok 
- Když už ten první je 1, tak ho automaticky bere a jsou mu další podmínky jedno 
- Logický součet
## Negace
- zápis - <code>!</code> 
- Všechno za ním je přesný opak 
## ekvivalence  
- zápis - <code>==</code>
- Když jsou obě nuly nebo obě jedničky 
<hr> 

# Trojúhelníková nerovnost

```java
/* Uživatel zadá 3 strany a program zjistí, jestli to může být trojúhelník a napíše to.*/
//otevřu scanner  
import java.util.Scanner;
 
public class Main 
{
	 public static void main(String[] args) { 
		 //vyvolám si scanner - !!!Důležité!!!  
		Scanner sc = new Scanner(System.in);  
		System.out.println("Zadej strany trojhelníku");  
		/*získávání velikostí stran 3x za sebou
		při kopírování kódu nesmím zapomenout na změnění proměnnných */
		System.out.print("Zadej 1. stranu ");  
		double a = sc.nextDouble();  
		System.out.print("Zadej 2. stranu ");  
		double b = sc.nextDouble();  
		System.out.print("Zadej 3. stranu "); 
		 double c = sc.nextDouble();  
		/* podmínka, která zjistí, jestli jsou strany vhodné  
		1) každá strana musí být větší než nula  
		2) součet dvou stran musí být větší než strana třetí */  
		if ((a+b>c && a+c>b && b+c>a) && a>0 && b>0 && c>0) { 
			System.out.println("Je to trojúhelník");
		} else {
			System.out.println("Není to trojúhelník"); 
		}  
		//zavřu scanner
		sc.close();
	}
}
```


[[poznámky z 10.2|předchozí]] [[poznámky z 10.3|následující]]