# JAVA Odev 9 Basit Kullanici Giris

```java
import java.util.Scanner;

public class KullaniciGirisi {

	public static void main(String[] args) {
		String inUserName;
		String inPassword;
		int secim;
		String userName = "patika";
		String password = "java123";

		Scanner scan = new Scanner(System.in);
		System.out.print("Kullanıcı Adını Giriniz : ");
		inUserName = scan.nextLine();
		System.out.print("Şifrenizi Giriniz : ");
		inPassword = scan.nextLine();

		if (userName.equals(inUserName) && password.equals(inPassword)) {
			System.out.println("Başarıyla giriş yaptınız..");
		} else {
			System.out.print(
					"Giriş yapamadınız!\nŞifrenizi Sıfırlamak ister misiniz?\nEvet için 1\nHayır için 2 tuşuna basınız : ");
			secim = scan.nextInt();
			switch (secim) {
				case 1:
					System.out.print("Yeni Şifrenizi Giriniz : ");
					inPassword = scan.next();
					if (inPassword.equals(password) || inPassword.equals(null)) {
						System.out.println("Şifre oluşturulamadı, lütfen başka şifre giriniz.");
						break;
					} else {
						System.out.println("Şifre oluşturuldu");
					}
				case 2:
					System.out.println("Teşekkür ederiz..");
					break;
				default:
					System.out.println("Bilinmeyen Seçim yaptınız");
			}
		}
		scan.close();
	}

}

```