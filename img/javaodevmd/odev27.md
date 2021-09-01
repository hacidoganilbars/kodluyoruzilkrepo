# JAVA Odev 27 Girilen Sayilardan En Buyuk ve En Kucuk Degerleri Bulma

```java

import java.util.Scanner;

public class MaxMinBulma {

	public static void main(String[] args) {
		int adet;
		int enBuyuk = 0;
		int enKucuk = 0;
		int sayi;
		Scanner scan = new Scanner(System.in);
		System.out.print("Kaç tane sayı gireceksiniz: ");
		adet = scan.nextInt();

		for (int i = 1; i <= adet; i++) {
			System.out.print(i + ". Sayıyı giriniz: ");
			sayi = scan.nextInt();
			if (sayi > enBuyuk) {
				enBuyuk = sayi;
			} else {
				enKucuk = sayi;
			}
		}
		System.out.println("En Büyük Sayı: " + enBuyuk);
		System.out.println("En Küçük Sayı: " + enKucuk);

		scan.close();
	}
}

```