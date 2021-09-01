# JAVA Odev 29 Yildizlarla Ters Ucgen Cizimi

```java
import java.util.Scanner;

public class TersUcgen {

	public static void main(String[] args) {

		int basamak;
		Scanner scan = new Scanner(System.in);
		System.out.print("Basamak Sayısı giriniz: ");
		basamak = scan.nextInt();
		System.out.println();

		for (int i = basamak; i > 0; i--) {
			for (int j = basamak - i; j > 0; j--) {
				System.out.print(" ");
			}

			for (int j = 2 * i - 1; j > 0; j--) {
				System.out.print("*");
			}
			System.out.println();
		}
		scan.close();

	}

}

```