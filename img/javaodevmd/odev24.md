# JAVA Odev 24 Java Yildizlar ile Baklava Dilimi

```java

import java.util.Scanner;

public class JavaYildiz {

	public static void main(String[] args) {
		int n;
		Scanner scan = new Scanner(System.in);
		System.out.print("Bir Sayı giriniz: ");
		n = scan.nextInt();

		for (int i = 1; i <= n; i++) {
			for (int j = 1; j <= (n - i); j++) {
				System.out.print(" ");
			}
			for (int j = 1; j <= (2 * i - 1); j++) {
				System.out.print("*");
			}

			System.out.println(" ");
		}
		for (int i = n - 1; i >= 1; i--) {
			for (int j = n - i; j >= 1; j--) {
				System.out.print(" ");
			}
			for (int j = (2 * i - 1); j >= 1; j--) {
				System.out.print("*");
			}

			System.out.println(" ");
		}
		scan.close();
	}
}

```