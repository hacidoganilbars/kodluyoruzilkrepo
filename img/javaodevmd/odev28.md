# JAVA Odev 28 Mukemmel Sayi

```java

import java.util.Scanner;

public class MukemmelSayi {

	public static void main(String[] args) {
		int sayi;
		int carpanToplam = 0;
		Scanner scan = new Scanner(System.in);
		System.out.print("Bir sayı giriniz: ");
		sayi = scan.nextInt();

		for (int i = 1; i < sayi; i++) {
			if (sayi % i == 0) {
				carpanToplam += i;
			}
		}
		if (carpanToplam == sayi) {
			System.out.println(sayi + " Mükemmel Sayıdır");
		} else {
			System.out.println(sayi + " Mükemmel Sayı Değildir!");
		}

		scan.close();
	}
}

```