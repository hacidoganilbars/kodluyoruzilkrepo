# JAVA Odev 26 Obeb Okek Bulma


```java

import java.util.Scanner;

public class EbobEkok {

	public static void main(String[] args) {
		int n1;
		int n2;
		int enkucuk;
		int ebob = 0;
		int sayac = 1;
		int carpim;
		Scanner scan = new Scanner(System.in);
		System.out.print("n1 sayısını giriniz: ");
		n1 = scan.nextInt();
		System.out.print("n2 sayısını giriniz: ");
		n2 = scan.nextInt();

		if (n1 > n2) {
			enkucuk = n2;
		} else {
			enkucuk = n1;
		}
		carpim = n1 * n2;
		while (carpim >= 1) {
			carpim--;
			sayac++;
			if (sayac % n1 == 0 && sayac % n2 == 0) {
				System.out.println(n1 + " ve " + n2 + " sayılarının Ekoku: " + sayac);
				break;
			}
		}

	/*	while (enkucuk >= 1) {
			sayac++;
			if (n1 % sayac == 0 && n2 % sayac == 0) {
				ebob = sayac;
			}
			enkucuk--;
		}
		System.out.println(n1 + " ve " + n2 + " sayılarının ebobu: " + ebob);

		while (enkucuk >= 1) {
			if (n1 % enkucuk == 0 && n2 % enkucuk == 0) {
				ebob = enkucuk;
				break;
			}
			enkucuk--;
		}
		System.out.println(n1 + " ve " + n2 + " sayılarının ebobu: " + ebob);
     */
		scan.close();
	}

}


```