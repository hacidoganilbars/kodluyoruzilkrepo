# JAVA Odev 19 4 ve 5'in kuvvetlerini bulma

```java
import java.util.Scanner;

public class DortVeBesinKuvvetleri {

	public static void main(String[] args) {
		int n;
		Scanner scan = new Scanner(System.in);
		System.out.print("Bir Sayı giriniz : ");
		n = scan.nextInt();
		System.out.println("4'ün kuvvetleri");
		for (int i = 1; i <= n; i *= 4) {
			System.out.println(i);
		}
		System.out.println("\n5'in kuvvetleri");
		for (int i = 1; i <= n; i *= 5) {
			System.out.println(i);
		}

		scan.close();
	}
}

```

