# JAVA Odev 19 4 ve 5'in katı sayıları bulma

```java
import java.util.Scanner;

public class DortVeBesinKuvvetleri {

	public static void main(String[] args) {
		int n;
		Scanner scan = new Scanner(System.in);
		System.out.print("Bir Sayı giriniz : ");
		n = scan.nextInt();

		for (int i = 0; i <= n; i += 20) {
			System.out.println(i);
		}

		scan.close();
	}
}

