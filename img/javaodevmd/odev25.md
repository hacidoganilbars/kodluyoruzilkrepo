# JAVA Odev 25 Basit ATM İşlemleri

```java

import java.util.Scanner;

public class AtmIslemleri {

	public static void main(String[] args) {
		String userName;
		String password;
		int right = 3;
		int balance = 1500;
		int select;
		Scanner scan = new Scanner(System.in);

		while (right >= 0) {
			System.out.print("Kullanıcı Adınız: ");
			userName = scan.nextLine();
			System.out.print("Parolanız: ");
			password = scan.nextLine();

			if (userName.equals("dogan") && password.equals("ozlem123")) {
				System.out.println("Merhaba Kod Banka Hoşgeldiniz!");

				do {
					System.out.println("1-Para yatırma\n" + "2-Para Çekme\n" + "3-Bakiye Sorgula\n" + "4-Çıkış Yap");
					System.out.print("Lütfen yapmak istediğiniz işlemi seçiniz : ");
					select = scan.nextInt();
					switch (select) {
					case 1:
						System.out.print("Para miktarı : ");
						int price = scan.nextInt();
						balance += price;
						break;
					case 2:
						System.out.print("Para miktarı : ");
						price = scan.nextInt();
						if (price > balance) {
							System.out.println("Bakiye yetersiz.");
						} else {
							balance -= price;
						}
						break;
					case 3:
						System.out.println("Bakiyeniz : " + balance);
						break;
					}
				} while (select != 4);
				System.out.println("Tekrar görüşmek üzere.");
				break;
			} else {
				right--;
				System.out.println("Hatalı kullanıcı adı veya şifre. Tekrar deneyiniz.");
				if (right == 0) {
					System.out.println("Hesabınız bloke olmuştur lütfen banka ile iletişime geçiniz.");
				} else {
					System.out.println("Kalan Hakkınız : " + right);
				}
			}
		}
		scan.close();

	}

}

```