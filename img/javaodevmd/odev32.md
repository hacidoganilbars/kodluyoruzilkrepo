# JAVA Odev 32 Palindrome Sayı

```java

import java.util.Scanner;

public class PalindromeSayi {

	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		System.out.print("Sayı Giriniz: ");
		int sayi = scan.nextInt();
		boolean sonuc = palindromeMu(sayi);
		System.out.println(sayi + " sayısı Palindrome Mu: " + sonuc);

		scan.close();

	}

	static boolean palindromeMu(int sayi) {
		int temp = sayi;
		int sonRakam = 0;
		int yeniSayi = 0;

		while (temp != 0) {
			sonRakam = temp % 10;
			yeniSayi = (yeniSayi * 10) + sonRakam;
			temp = temp / 10;
		}
		if (sayi == yeniSayi) {
			return true;
		} else {
			return false;
		}
	}
}

```