# JAVA Odev 6 Vucut Kitle Indeksi Hesaplama

```java

import java.util.Scanner;

public class VucutKutleIndexHesap {

	public static void main(String[] args) {

		double boy;
		int kilo;
		double vucutKitleIndexi;

		Scanner scan = new Scanner(System.in);
		System.out.print("Lütfen boyunuzu (metre cinsinde) giriniz : ");
		boy = scan.nextDouble();
		System.out.print("Lütfen kilonuzu giriniz : ");
		kilo = scan.nextInt();

		vucutKitleIndexi = kilo / (boy * boy);
		System.out.println("Vücut Kitle İndeksiniz : " + vucutKitleIndexi);

		scan.close();

	}
}

```