# JAVA Odev 23 Harmonik Seri Bulan Program


```java
import java.util.Scanner;

public class HarmonikSeri {

	public static void main(String[] args) {

		int n;
		double sonuc = 0.0;
		Scanner scan = new Scanner(System.in);
		System.out.print("Bir Sayı Giriniz: ");
		n = scan.nextInt();
		for (int i = 1; i <= n; i++) {
			sonuc += (1.0 / i);
		}

		System.out.println("Harmonik Seri Sonucu: " + sonuc);
		
		scan.close();

	}

}

```