# JAVA Odev 5 Merkez Açısı ve Yarıçapı verilen Daire Diliminin Alanını Hesaplama


```java
import java.util.Scanner;

public class DaireDilimAlanHesap {

	public static void main(String[] args) {

		double pi = 3.14;
		int yaricap;
		int aci;
		double diliminAlani;

		Scanner scan = new Scanner(System.in);

		System.out.print("Dairenin yarıçapını giriniz: ");
		yaricap = scan.nextInt();

		System.out.print("Merkez açısını giriniz: ");
		aci = scan.nextInt();

		diliminAlani = (pi * (yaricap * yaricap) * aci) / 360;

		System.out.println("Daire diliminin alanı: " + diliminAlani);

		scan.close();
	}
}

```