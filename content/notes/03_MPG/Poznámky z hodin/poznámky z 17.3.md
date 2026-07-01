---
date: 2026-03-17
author: n7x3n
---
# Hvězdičkový trojúhelník
```java
/* Vytvořte program, který kreslí "trojúhelník z hvězdiček". Uživatel zadá kolik řádků má mít. Každý řádek přeskočí.*/ 
import java.util.Scanner;
public class Main 
{
	 public static void main(String[] args) {
		Scanner sc = new
		Scanner(System.in);System.out.println("Kolik mám napsat řádků hvězdiček?");
		int radku = sc.nextInt();
		for (int i = 1;i <= radku ; i++ ) {  
	        if (i > radku) break;  
	        for (int j = 1;j <= i ; j++ ) {  
	            if (i % 2 == 0) continue;  
	            System.out.print("*");  
	        }  
	        System.out.println();  
	    }
     
	    sc.close();         
	}
}
```

---
# 3 Druhy Chyb
## 1. Syntaktická Chyba
- záměna velkého a malého písmene, chybějící ; , překlepy...
- "posere se hned na startu"
## 2. Běhová Chyba
- chyba v proměnných, neotevřený scanner....
- "posere se v průběhu"
## 3. Logická Chyba
- špatně zapsaný výpočet...
- "Neposere se, ale výsledek je na hovno"
---
# Bartův program
```java
/*Bartův program */
//import scanneru
import java.util.Scanner;
 public class Main 
 {
	 public static void main(String[] args) {
		//vytvořím si scanner
		Scanner sc = new Scanner(System.in);
		//ptám se, kolik mám napsat řádků
		System.out.println("Kolik mám napsat řádků?");
		//nahraju to do proměnné
		int kolikrat = sc.nextInt();
		//ptám se, co mám napsat
		System.out.println("Co mám napsat?");
		//řeknu, že chci znovu scanner
		sc.nextLine();
		//nahraju obsah scanneru do Stringu
		String coMamNapsat = sc.nextLine ();
		//podmínka nastaví opakování 
		for (int i = 1;i <= kolikrat ; i++ ) {
			//vypíšu obě dvě proměnné
			System.out.println(i+". "+coMamNapsat);  
		}
	}
}
```


[[poznámky z 10.3|předchozí]] [[poznámky z 24.3|následující]]