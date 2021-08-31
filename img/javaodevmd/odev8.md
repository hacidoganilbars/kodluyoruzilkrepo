# JAVA Odev 8 Switch Case ile Basit Hesap Makinesi

```java
import java.util.Scanner;

public class SwitchCaseHesapMakinesi {

	public static void main(String[] args) {

		int sayi1, sayi2, secim;

		Scanner scan = new Scanner(System.in);
		System.out.print("İlk sayıyı giriniz : ");
		sayi1 = scan.nextInt();

		System.out.print("İlk sayıyı giriniz : ");
		sayi2 = scan.nextInt();

		System.out.print("Seçiminizi yapınız\n1 - Toplama\n2 - Çıkarma\n3 - Çarpma\n4 - Bölme\nSeçiminiz : ");
		secim = scan.nextInt();

		switch (secim) {
		case 1:
			System.out.println("Sonuç : " + (sayi1 + sayi2));
			break;
		case 2:
			System.out.println("Sonuç : " + (sayi1 - sayi2));
			break;
		case 3:
			System.out.println("Sonuç : " + (sayi1 * sayi2));
			break;
		case 4:
			if (sayi2 != 0) {
				System.out.println("Sonuç : " + (sayi1 / sayi2));
				break;
			} else {
				System.out.println("Bölüm sıfır olamaz");
			}
		default:
			System.out.println("Tekrar deneyiniz...");
		}

		scan.close();

	}

}

