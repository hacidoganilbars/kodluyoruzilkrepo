# JAVA Odev 7 Manav Hesap

```java
import java.util.Scanner;

public class ManavKasa {

	public static void main(String[] args) {

		double armut = 2.14;
		double elma = 3.67;
		double domates = 1.11;
		double muz = 0.95;
		double patlican = 5.00;
		double toplamTutar;
		int kilo;

		Scanner scan = new Scanner(System.in);
		System.out.print("Armut Kaç Kilo ? : ");
		kilo = scan.nextInt();
		armut *= kilo;

		System.out.print("Elma Kaç Kilo ? : ");
		kilo = scan.nextInt();
		elma *= kilo;

		System.out.print("Domates Kaç Kilo ? : ");
		kilo = scan.nextInt();
		domates *= kilo;

		System.out.print("Muz Kaç Kilo ? : ");
		kilo = scan.nextInt();
		muz *= kilo;

		System.out.print("Patlıcan Kaç Kilo ? : ");
		kilo = scan.nextInt();
		patlican *= kilo;

		toplamTutar = elma + armut + domates + muz + patlican;
		System.out.println("Toplam Tutar : " + toplamTutar);

		scan.close();

	}
}

```