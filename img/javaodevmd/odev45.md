# JAVA Odev 45 Dizideki Elemanların Frekansını Bulma

## DizidekiElemanlarinFrekansi
```java
import java.util.Arrays;

public class DizidekiElemanlarinFrekansi {

	public static void main(String[] args) {

		int arr[] = { 10, 20, 20, 10, 10, 20, 5, 20 };

		int count = 0;
		Arrays.sort(arr);
		
		for (int i = 0; i < arr.length; i++) {
			count = 0;
			for (int j = 0; j < arr.length; j++) {
				if (arr[i] == arr[j]) {
					count++;
				}
			}

			if (i == 0 && arr[i + 1] == arr[i]) {
				System.out.println(arr[i] + " sayısı " + count + " kere tekrar edildi");
			}
			if (i == 0 && arr[i + 1] != arr[i]) {
				System.out.println(arr[i] + " sayısı " + count + " kere tekrar edildi");
			}
			if (i != 0 && arr[i - 1] != arr[i]) {
				System.out.println(arr[i] + " sayısı " + count + " kere tekrar edildi");
			}

		}
	}
}

```

## Console
```console
5 sayısı 1 kere tekrar edildi
10 sayısı 3 kere tekrar edildi
20 sayısı 4 kere tekrar edildi

```