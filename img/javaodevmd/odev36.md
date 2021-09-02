# JAVA Odev 36 Recursive Metod ile Desen

```java

import java.util.Scanner;

public class DeseneGoreRecursive {

	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		System.out.print("Sayı giriniz: ");
		int sayi = scan.nextInt();
		recursiveDesen(sayi);

		scan.close();

	}
	
	//Boyle odev olmaz olsun :D
	static int recursiveDesen(int sayi) {
		int azalanTaraf = sayi;
		System.out.print(azalanTaraf + " ");
		if (azalanTaraf <= 0) {
			return azalanTaraf;
		}
		int artanTaraf = recursiveDesen(sayi - 5) + 5;
		System.out.print(artanTaraf + " ");
		return artanTaraf;
	}
}

```