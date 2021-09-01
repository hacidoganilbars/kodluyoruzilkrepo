# JAVA Odev 16 Artık Yıl Hesaplama

```java
import java.util.Scanner;

public class ArtikYilHesap {

	public static void main(String[] args) {

		int yil = 0;
		Scanner scan = new Scanner(System.in);
		System.out.print("Yıl Giriniz : ");
		yil = scan.nextInt();

		if (yil % 100 == 0) {
			if (yil % 400 == 0) {
				System.out.println(yil + " bir artık yıldır");
			} else {
				System.out.println(yil + " bir artık yıl değildir");
			}
		} else if (yil % 100 != 0 && yil % 4 == 0) {
			System.out.println(yil + " bir artık yıldır");
		} else {
			System.out.println(yil + " bir artık yıl değildir");
		}

		scan.close();
	}
}

```