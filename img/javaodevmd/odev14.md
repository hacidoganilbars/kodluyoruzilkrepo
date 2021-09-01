# JAVA Odev 14 Ucak Bileti Fiyat Hesaplama

```java

import java.util.Scanner;

public class UcakBiletFiyatHesap {

	public static void main(String[] args) {
		int yas, km, tip;
		double fiyat;
		double yasIndirimOrani = 0;

		Scanner scan = new Scanner(System.in);
		System.out.print("Mesafeyi km cinsinden giriniz: ");
		km = scan.nextInt();
		System.out.print("Yaşınızı giriniz: ");
		yas = scan.nextInt();
		System.out.print("Yolculuk tipini giriniz (1 => Tek Yön , 2 => Gidiş Dönüş ): ");
		tip = scan.nextInt();

		fiyat = km * 0.10;

		if (yas > 0 && km > 0 && (tip == 1 || tip == 2)) {

			if (yas > 65) {
				yasIndirimOrani = 0.30;
			} else if (yas > 11 && yas < 24) {
				yasIndirimOrani = 0.10;

			} else if (yas < 12) {
				yasIndirimOrani = 0.50;
			}
			fiyat = fiyat - fiyat * yasIndirimOrani;
			if (tip == 1) {
				fiyat = fiyat * 1;
			} else if (tip == 2) {
				fiyat = (fiyat - fiyat * 0.20) * 2;
			}

			System.out.println("Toplam Tutar: " + fiyat);

		} else {
			System.out.println("Hatalı Veri Girdiniz !");
		}

		scan.close();
	}
}

```