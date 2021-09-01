# JAVA Odev 20 n'in r'li kombinasyonu

```java

import java.util.Scanner;

public class KombinasyonHesap {

	public static void main(String[] args) {
		int n;
		int r;
		int nfak = 1;
		int rfak = 1;
		int nrfak = 1;
		double combinasyon;
		Scanner scan = new Scanner(System.in);
		System.out.print("n eleman sayısını giriniz : ");
		n = scan.nextInt();
		System.out.print("r eleman sayısını giriniz : ");
		r = scan.nextInt();

		for (int i = 1; i <= n; i++) {
			nfak *= i;
		}
		for (int i = 1; i <= r; i++) {
			rfak *= i;
		}
		for (int i = 1; i <= (n - r); i++) {
			nrfak *= i;
		}

		combinasyon = nfak / (rfak * nrfak);
		System.out.println("Kombinasyon Sonucu: " + combinasyon);

		scan.close();
	}
}

```