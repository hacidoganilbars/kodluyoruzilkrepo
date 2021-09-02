# JAVA Odev 34 Recursive metod ile Uslu Sayilar

```java
import java.util.Scanner;

public class RecursiveUsluSayi {

	public static void main(String[] args) {

		int sayi1;
		int sayi2;

		Scanner scan = new Scanner(System.in);

		System.out.print("Taban değeri giriniz : ");
		sayi1 = scan.nextInt();
		System.out.print("Üs değerini giriniz : ");
		sayi2 = scan.nextInt();

		int result = recursiveUsAl(sayi1, sayi2);
		System.out.println("Sonuç : " + result);

		scan.close();

	}

	static int recursiveUsAl(int a, int b) {
		if (b == 0) {
			return 1;
		}
		return a * recursiveUsAl(a, b - 1);
	}

}


```