# JAVA Odev 4 Kuralli Taksimetre Ucreti


```java
import java.util.Scanner;

public class KuralliTaksimetre {

	public static void main(String[] args) {

		int taksimetreAcilisUcreti = 10;
		double kmBasinaEklenenUcret = 2.20;
		int minTutar = 20;

		int gidilenKm;

		double odenecekTutar;

		Scanner scan = new Scanner(System.in);
		System.out.print("Gidilen KM'yi giriniz: ");
		gidilenKm = scan.nextInt();

		odenecekTutar = taksimetreAcilisUcreti + gidilenKm * kmBasinaEklenenUcret;

		odenecekTutar = odenecekTutar < minTutar ? minTutar : odenecekTutar;

		System.out.println("Ödenecek Ücret: " + odenecekTutar);
		
		scan.close();
	}
}

```
