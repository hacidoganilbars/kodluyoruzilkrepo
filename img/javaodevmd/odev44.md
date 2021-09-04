# JAVA Odev 44 Dizideki Elemanları Sıralama


## SayiDizisindedeElemanlariSiralama
```java
import java.util.Arrays;
import java.util.Scanner;

public class SayiDizisindedeElemanlariSiralama {

	public static void main(String[] args) {
		int uzunluk;
		int[] arr;
		Scanner scan = new Scanner(System.in);
		System.out.print("Dizinin boyutu n : ");
		uzunluk = scan.nextInt();
		arr = new int[uzunluk];
		System.out.println("Dizinin elemanlarını giriniz : ");
		for (int i = 0; i < arr.length; i++) {
			System.out.print((i + 1) + ". Elemanı : ");
			arr[i] = scan.nextInt();
		}

		Arrays.sort(arr);
		System.out.print("Sıralama: ");
		for (int i : arr) {
			System.out.print(i + " ");
		}

		scan.close();
	}
}

```

## Console
```console
Dizinin boyutu n : 5
Dizinin elemanlarını giriniz : 
1. Elemanı : 12
2. Elemanı : 7
3. Elemanı : -33
4. Elemanı : 0
5. Elemanı : 1
Sıralama: -33 0 1 7 12 

```