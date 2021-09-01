# JAVA Odev 13 Ay ve Gun ile Burc Bulma Programi

```java

import java.util.Scanner;

public class BurcBulma {

	public static void main(String[] args) {

		int ay, gun;
		Scanner scan = new Scanner(System.in);
		System.out.print("Ay giriniz: ");
		ay = scan.nextInt();
		System.out.print("Gün giriniz: ");
		gun = scan.nextInt();
		String burc = "";

		if ((gun > 0 && gun < 32) && (ay > 0 && ay < 13)) {

			if (ay == 1) {
				if (gun < 22) {
					burc = "Oğlak";
				} else {
					burc = "Kova";
				}
			} else if (ay == 2) {
				if (gun < 20) {
					burc = "Kova";
				} else {
					burc = "Balık";
				}
			} else if (ay == 3) {
				if (gun < 21) {
					burc = "Balık";
				} else {
					burc = "Koç";
				}
			} else if (ay == 4) {
				if (gun < 21) {
					burc = "Koç";
				} else {
					burc = "Boğa";
				}
			} else if (ay == 5) {
				if (gun < 23) {
					burc = "Boğa";
				} else {
					burc = "İkizler";
				}
			}
			if (ay == 6) {
				if (gun < 23) {
					burc = "İkizler";
				} else {
					burc = "Yengeç";
				}
			} else if (ay == 7) {
				if (gun < 23) {
					burc = "Yengeç";
				} else {
					burc = "Aslan";
				}
			} else if (ay == 8) {
				if (gun < 23) {
					burc = "Aslan";
				} else {
					burc = "Başak";
				}
			} else if (ay == 9) {
				if (gun < 23) {
					burc = "Başak";
				} else {
					burc = "Terazi";
				}
			} else if (ay == 10) {
				if (gun < 23) {
					burc = "Terazi";
				} else {
					burc = "Akrep";
				}
			} else if (ay == 11) {
				if (gun < 22) {
					burc = "Akrep";
				} else {
					burc = "Yay";
				}
			} else {
				if (gun < 22) {
					burc = "Yay";
				} else {
					burc = "Oğlak";
				}
			}
		} else {
			System.out.println("Geçersiz gün veya ay girdiniz!");
		}

		System.out.println("Burcunuz: " + burc);
		scan.close();
	}
}

```