# JAVA Odev 1

```java

import java.util.Scanner;

public class OrtalamaHesap {
	public static void main(String[] args) {

		int matematik, fizik, kimya, turkce, tarih, muzik;

		Scanner scan = new Scanner(System.in);

		System.out.print("Matematik notunu giriniz: ");
		matematik = scan.nextInt();

		System.out.print("Fizik notunu giriniz: ");
		fizik = scan.nextInt();

		System.out.print("Kimya notunu giriniz: ");
		kimya = scan.nextInt();

		System.out.print("Türkçe notunu giriniz: ");
		turkce = scan.nextInt();

		System.out.print("Tarih notunu giriniz: ");
		tarih = scan.nextInt();

		System.out.print("Müzik notunu giriniz: ");
		muzik = scan.nextInt();

		int toplam = matematik + fizik + kimya + turkce + tarih + muzik;

		double sonuc = toplam / 6;

		String gectiMi = sonuc > 60.0 ? "Sınıfı Geçti" : "Sınıfta Kaldı";

		System.out.println(sonuc + " ortalamasıyla : " + gectiMi);

		scan.close();
	}
}

```
  