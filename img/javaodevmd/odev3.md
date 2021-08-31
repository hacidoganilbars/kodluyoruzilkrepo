# JAVA Odev 3 Kenarlari Bilinen Ucgen Alani Hesap


```java

import java.util.Scanner;

public class KenarlariVerilenUcgenAlan {

	public static void main(String[] args) {

		int kenar1, kenar2, kenar3;
		double u;
		double alan;
		int cevre;

		Scanner scan = new Scanner(System.in);

		System.out.print("Üçgenin 1. kenarını giriniz: ");
		kenar1 = scan.nextInt();

		System.out.print("Üçgenin 2. kenarını giriniz: ");
		kenar2 = scan.nextInt();

		System.out.print("Üçgenin 3. kenarını giriniz: ");
		kenar3 = scan.nextInt();

		cevre = kenar1 + kenar2 + kenar3;

		u = cevre / 2;

		alan = Math.sqrt(u * (u - kenar1) * (u - kenar2) * (u - kenar3));

		System.out.println("Kenarları: " + kenar1 + ", " + kenar2 + ", " + kenar3 + ", olan üçgenin");
		System.out.println("Çevresi: " + cevre);
		System.out.println("Alanı: " + alan);
		
		scan.close();
	}
}

```