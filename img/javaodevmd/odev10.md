# JAVA Odev 10 Ogrenci Ortalama Gecme Kalma

```java
import java.util.Scanner;

public class OrtalamayaGoreOgrenciHesap {

	public static void main(String[] args) {
		int matematik, fizik, turkce, kimya, muzik;
		double ortalama;

		Scanner scan = new Scanner(System.in);
		System.out.print("Matematik Notunu Giriniz: ");
		matematik = scan.nextInt();

		System.out.print("Fizik Notunu Giriniz: ");
		fizik = scan.nextInt();

		System.out.print("Türkçe Notunu Giriniz: ");
		turkce = scan.nextInt();

		System.out.print("Kimya Notunu Giriniz: ");
		kimya = scan.nextInt();

		System.out.print("Muzik Notunu Giriniz: ");
		muzik = scan.nextInt();

		if ((matematik < 0) || (matematik > 100)) {
			matematik = 0;
		} else if ((fizik < 0) || (fizik > 100)) {
			fizik = 0;
		} else if ((turkce < 0) || (turkce > 100)) {
			turkce = 0;
		} else if ((kimya < 0) || (kimya > 100)) {
			fizik = 0;
		} else if ((muzik < 0) || (muzik > 100)) {
			muzik = 0;
		}

		ortalama = (matematik + fizik + turkce + kimya + muzik) / 5;

		if (ortalama >= 55) {
			System.out.println("Tebrikler Geçtiniz");
		} else {
			System.out.println("Kaldınız");
		}

		System.out.println("Ortalamanız: " + ortalama);
		scan.close();
	}
}

```