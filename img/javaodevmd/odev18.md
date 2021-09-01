# JAVA Odev 18 Girilen sayilardan 4ün katlarını Toplar

```java

import java.util.Scanner;

public class DordunKatlariToplam {

	public static void main(String[] args) {
		int sayi;
		int toplam = 0;

		Scanner scan = new Scanner(System.in);

		do {
			System.out.print("Sayı giriniz: ");
			sayi = scan.nextInt();
			if (sayi > 0 && sayi % 4 == 0) {
				toplam += sayi;
			}
		} while (sayi > 0);

		System.out.println("Dördün katı olan sayıların toplamı: " + toplam);

		scan.close();
	}
}

