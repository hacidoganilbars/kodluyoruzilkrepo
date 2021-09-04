# JAVA Odev 41 Girilen Sayiya En Yakin En Buyuk ve En Kucuk Sayi

## GirilenSayiyaEnYakinBuyukKucuk
```java
import java.util.Arrays;
import java.util.Scanner;

public class GirilenSayiyaEnYakinBuyukKucuk {

	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		int arr[] = { 15, 12, 788, 1, -1, -778, 2, 0 };
		int list[] = new int[arr.length];

		int enKucuk = 0;
		int enBuyuk = 0;

		System.out.print("Bir saayı giriniz örnek 5 : ");
		int sayi = scan.nextInt();

		for (int i = 0; i < arr.length; i++) {
			list[i] = Math.abs(arr[i]);
		}

		Arrays.sort(list);

		for (int i = 0; i < list.length; i++) {
			if (sayi > list[i]) {
				enKucuk = list[i];
				enBuyuk = list[i + 1];
			}

		}

		System.out.println(enKucuk);
		System.out.println(enBuyuk);

		scan.close();
	}

}

```

## Console
```console
Bir saayı giriniz örnek 5 : 5
2
12

```