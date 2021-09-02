# JAVA Odev 35 Recursive Asal Sayı

```java

import java.util.Scanner;

public class RecursiveAsal {

	static boolean isPrime(int x, int a) {

		if (a == 2) {
			return !(x % a == 0);
		} else {
			return (x % a != 0) && isPrime(x, a - 1);
		}
	}

	static boolean isPrime(int x) {

		if (x <= 1) {
			return false;
		}

		if (x == 2) {
			return true;
		} else {
			int a = x - 1;
			return isPrime(x, a);
		}
	}

	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);
		System.out.print("Sayi giriniz: ");
		int num = scan.nextInt();

		if (isPrime(num)) {
			System.out.println(num + " sayısı ASALDIR !");
		} else {
			System.out.println(num + " sayısı ASAL değildir !");
		}

		scan.close();
	}
}


```