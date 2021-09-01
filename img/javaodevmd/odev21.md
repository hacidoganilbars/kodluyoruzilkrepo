# JAVA Odev 21 Us Alma İşlemi

```java

import java.util.Scanner;

public class UsAlma {

	public static void main(String[] args) {
		int n, k;
		int total = 1;

		Scanner scan = new Scanner(System.in);
		System.out.print("Üssü alınaca sayıyı giriniz: ");
		n = scan.nextInt();
		System.out.print("Üs olacak sayıyı giriniz: ");
		k = scan.nextInt();
		for (int i = 1; i <= k; i++) {
			total *= n;
		}

		System.out.println(n + "^" + k + " = " + total);
		scan.close();
	}
}

```