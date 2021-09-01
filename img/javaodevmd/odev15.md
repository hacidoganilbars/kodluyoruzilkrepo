# JAVA Odev 15 Çin Zodyağı

```java
import java.util.Scanner;

public class CinZodyagi {

	public static void main(String[] args) {

		int dogumYili;
		int zodyak;
		String sonuc;

		Scanner scan = new Scanner(System.in);
		System.out.print("Doğum yılınızı giriniz: ");
		dogumYili = scan.nextInt();

		zodyak = dogumYili % 12;

		if (zodyak == 0) {
			sonuc = "Maymun";
		} else if (zodyak == 1) {
			sonuc = "Horoz";
		} else if (zodyak == 2) {
			sonuc = "Köpek";
		} else if (zodyak == 3) {
			sonuc = "Domuz";
		} else if (zodyak == 4) {
			sonuc = "Fare";
		} else if (zodyak == 5) {
			sonuc = "Öküz";
		} else if (zodyak == 6) {
			sonuc = "Kaplan";
		} else if (zodyak == 7) {
			sonuc = "Tavşan";
		} else if (zodyak == 8) {
			sonuc = "Ejderha";
		} else if (zodyak == 9) {
			sonuc = "Yılan";
		} else if (zodyak == 10) {
			sonuc = "At";
		} else {
			sonuc = "Koyun";
		}

		System.out.println("Çin Zodyağı Burcunuz: " + sonuc);
		scan.close();
	}

}

```