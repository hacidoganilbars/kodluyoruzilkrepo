# JAVA Odev 11 Hava Durumuna Gore Aktivite Oneri

```java
import java.util.Scanner;

public class HavaSicakligiEtkinlik {

	public static void main(String[] args) {

		int sicaklik;
		Scanner scan = new Scanner(System.in);
		System.out.print("Sıcaklığı giriniz: ");
		sicaklik = scan.nextInt();

		if (sicaklik > 25) {
			System.out.println("Yüzmeye gidebilirsin");
		} else if (sicaklik <= 25 && sicaklik >= 10) {
			if (sicaklik < 15) {
				System.out.println("Sinemaya gidebilirsin");
			}
			System.out.println("Pikniğe gidebilirsin");
		} else if (sicaklik > 5 && sicaklik < 15) {
			System.out.println("Sinemaya gidebilirsin");
		} else {
			System.out.println("Kayak yapabilirsin");
		}
		scan.close();
	}
}

```