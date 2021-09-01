# JAVA Odev 17  3 e ve 4 e bölen Sayıların ortalaması
## Sıfırdan Girilen sayıya kadar olan sayılardan 3'e ve 4'e tam bölünen sayıların ortalaması 

```java
import java.util.Scanner;

public class GirilenSayiyaKadarUcVeDordeBolunenSayilarinOrtalamasi {

	public static void main(String[] args) {
		int sayi;
		int toplam = 0;
		int sayac = 0;

		Scanner scan = new Scanner(System.in);

		System.out.print("Bir Sayı Giriniz: ");
		sayi = scan.nextInt();

		for (int i = 0; i <= sayi; i++) {
			if (i % 12 == 0) {
				toplam += i;
				sayac++;
			}
		}
		System.out.println("3 e ve 4 e bölünen sayıların ortalaması: " + (toplam / sayac));
		scan.close();
	}
}

```