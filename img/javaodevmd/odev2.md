#JAVA Odev 2 KDV HESAP


```java
import java.util.Scanner;

public class KdvTutarHesap {

	public static void main(String[] args) {

		double tutar, kdvLiFiyat, kdvTutari;
		double kdvOrani;

		Scanner scan = new Scanner(System.in);
		System.out.print("Tutarı Giriniz: ");
		tutar = scan.nextDouble();
		
		tutar = tutar<0 ? tutar*-1:tutar;
		
		kdvOrani = tutar > 1000.0 ? 0.08 : 0.18;

		kdvTutari = tutar * kdvOrani;
		kdvLiFiyat = tutar + kdvTutari;

		System.out.println("KDV'siz tutar: " + tutar);
		System.out.println("KDV Oranı: " + kdvOrani);
		System.out.println("KDV Tutarı: " + kdvTutari);
		System.out.println("KDV'li Tutar: " + kdvLiFiyat);

		scan.close();
	}
}

```