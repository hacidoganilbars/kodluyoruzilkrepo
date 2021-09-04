# JAVA Odev 40 Dizideki Sayilarin Harmonik Ortalamasi

## DizidekiSayilarinHarmonikOrtalamasi

```java

public class DizidekiSayilarinHarmonikOrtalamasi {

	public static void main(String[] args) {

		int[] arr = { 1, 2, 3, 4, 5, 6, 7 };

		double harmonikSeri = 0.0;
		for (int i = 0; i < arr.length; i++) {
			harmonikSeri += (1.0 / arr[i]);
		}

		double harmonikOrtalama = arr.length / harmonikSeri;
		System.out.println(harmonikOrtalama);

	}

}

```

## Console
```console
2.6997245179063363

```