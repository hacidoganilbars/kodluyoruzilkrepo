# JAVA Odev 43 Dizi İçerisindeki Tekrar eden Çift Sayilari Bulma

## ArrayIcersindeTekrarEdenCiftSayilar

```java

import java.util.Arrays;

public class ArrayIcersindeTekrarEdenCiftSayilar {

	public static void main(String[] args) {
		int arr[] = { 2, 1, 8, 3, 4, 8, 4, 2, 2, 3, 6, 7, 6, 1, 7, 8 };
		int cift[] = new int[arr.length];
		int startIndex = 0;
		for (int i = 0; i < arr.length; i++) {
			for (int j = 0; j < arr.length; j++) {
				if (i != j && arr[i] % 2 != 1 || arr[j] % 2 != 1 && arr[i] == arr[j]) {
					if (!isFind(cift, arr[i])) {
						cift[startIndex++] = arr[i];
					}
					break;
				}

			}
		}

		for (int i : cift) {
			if (i != 0) {
				System.out.print(i + " ");
			}
		}
	}

	static boolean isFind(int[] arr, int value) {
		for (int i : arr) {
			if (i == value) {
				return true;
			}
		}
		return false;
	}

}

```

## Console
```console
2 8 4 6 

```