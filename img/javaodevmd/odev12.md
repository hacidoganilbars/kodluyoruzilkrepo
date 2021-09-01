# JAVA Odev 12 UC(3) Sayıyı Kucukten Buyuke Siralama

```java

import java.util.Scanner;

public class UcSayiKucuktenBuyuge {

	public static void main(String[] args) {
		
		int a, b, c;

		Scanner scan = new Scanner(System.in);
		System.out.print("1.Sayıyı Giriniz a = ");
		a = scan.nextInt();
		System.out.print("2.Sayıyı Giriniz b = ");
		b = scan.nextInt();
		System.out.print("3.Sayıyı Giriniz c = ");
		c = scan.nextInt();

		if (a < b && a < c) {
			if (b < c) {
				System.out.println("a < b < c");
			} else {
				System.out.println("a < c < b");
			}
		} else if (b < a && b < c) {
			if (a < c) {
				System.out.println("b < a < c");
			} else {
				System.out.println("b < c < a");
			}
		} else {
			if (b < a) {
				System.out.println("c < b < a");
			} else {
				System.out.println("c < a < b");
			}
		}

		scan.close();
	}

}

```
