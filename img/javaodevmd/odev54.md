# JAVA Odev 54 Sanal Mağaza

## Product
```java

public abstract class Product {
	private int id;
	private double price;
	private double discountRate;
	private int stock;
	private String productName;
	private int storage;
	private double inch;
	private int ram;
	private Brand brand;

	public Product(int id, double price, double discountRate, int stock, String productName, int storage, double inch,
			 int ram, Brand brand) {
		this.id = id;
		this.price = price;
		this.discountRate = discountRate;
		this.stock = stock;
		this.productName = productName;
		this.storage = storage;
		this.inch = inch;
		this.ram = ram;
		this.brand = brand;
	}

	public int getId() {
		return id;
	}

	public void setId(int id) {
		this.id = id;
	}

	public double getPrice() {
		return price;
	}

	public void setPrice(double price) {
		this.price = price;
	}

	public double getDiscountRate() {
		return discountRate;
	}

	public void setDiscountRate(double discountRate) {
		this.discountRate = discountRate;
	}

	public int getStock() {
		return stock;
	}

	public void setStock(int stock) {
		this.stock = stock;
	}

	public String getProductName() {
		return productName;
	}

	public void setProductName(String productName) {
		this.productName = productName;
	}

	public int getStorage() {
		return storage;
	}

	public void setStorage(int storage) {
		this.storage = storage;
	}

	public double getInch() {
		return inch;
	}

	public void setInch(double inch) {
		this.inch = inch;
	}

	public int getRam() {
		return ram;
	}

	public void setRam(int ram) {
		this.ram = ram;
	}

	public Brand getBrand() {
		return brand;
	}

	public void setBrand(Brand brand) {
		this.brand = brand;
	}

}

```

## Brand
```java

public abstract class Product {
	private int id;
	private double price;
	private double discountRate;
	private int stock;
	private String productName;
	private int storage;
	private double inch;
	private int ram;
	private Brand brand;

	public Product(int id, double price, double discountRate, int stock, String productName, int storage, double inch,
			 int ram, Brand brand) {
		this.id = id;
		this.price = price;
		this.discountRate = discountRate;
		this.stock = stock;
		this.productName = productName;
		this.storage = storage;
		this.inch = inch;
		this.ram = ram;
		this.brand = brand;
	}

	public int getId() {
		return id;
	}

	public void setId(int id) {
		this.id = id;
	}

	public double getPrice() {
		return price;
	}

	public void setPrice(double price) {
		this.price = price;
	}

	public double getDiscountRate() {
		return discountRate;
	}

	public void setDiscountRate(double discountRate) {
		this.discountRate = discountRate;
	}

	public int getStock() {
		return stock;
	}

	public void setStock(int stock) {
		this.stock = stock;
	}

	public String getProductName() {
		return productName;
	}

	public void setProductName(String productName) {
		this.productName = productName;
	}

	public int getStorage() {
		return storage;
	}

	public void setStorage(int storage) {
		this.storage = storage;
	}

	public double getInch() {
		return inch;
	}

	public void setInch(double inch) {
		this.inch = inch;
	}

	public int getRam() {
		return ram;
	}

	public void setRam(int ram) {
		this.ram = ram;
	}

	public Brand getBrand() {
		return brand;
	}

	public void setBrand(Brand brand) {
		this.brand = brand;
	}

}

```

## Notebook
```java

public class Notebook extends Product{

	public Notebook(int id, double price, double discountRate, int stock, String productName, int storage, double inch,
			 int ram,Brand brand) {
		super(id, price, discountRate, stock, productName, storage, inch, ram,brand);
	}

}

```

## MobilePhone
```java

public class MobilePhone extends Product {

	private String color;
	private int batteryPow;

	public MobilePhone(int id, double price, double discountRate, int stock, String productName, int storage,
			double inch, int batteryPow, int ram, Brand brand, String color) {
		super(id, price, discountRate, stock, productName, storage, inch, ram, brand);
		this.color = color;
		this.batteryPow = batteryPow;
	}

	public String getColor() {
		return color;
	}

	public void setColor(String color) {
		this.color = color;
	}

	public int getBatteryPow() {
		return batteryPow;
	}

	public void setBatteryPow(int batteryPow) {
		this.batteryPow = batteryPow;
	}

}

```

## PatikaStore
```java

import java.util.ArrayList;
import java.util.Scanner;
import java.util.TreeSet;

public class PatikaStore {

	Scanner scan = new Scanner(System.in);

	public void run() {

		// Samsung, Lenovo, Apple, Huawei, Casper, Asus, HP, Xiaomi, Monster

		Brand samsung = new Brand(1, "Samsung");
		Brand lenovo = new Brand(2, "Lenovo");
		Brand apple = new Brand(3, "Apple");
		Brand huawei = new Brand(4, "Huawei");
		Brand casper = new Brand(5, "Casper");
		Brand asus = new Brand(6, "Asus");
		Brand hp = new Brand(7, "HP");
		Brand xiaomi = new Brand(8, "Xiaomi");
		Brand monster = new Brand(9, "Monster");

		TreeSet<Brand> liste = new TreeSet<>();
		liste.add(samsung);
		liste.add(lenovo);
		liste.add(apple);
		liste.add(huawei);
		liste.add(casper);
		liste.add(asus);
		liste.add(hp);
		liste.add(xiaomi);
		liste.add(monster);

		Notebook noteHuawei = new Notebook(1, 7000.0, 0.20, 10, "HUAWEI Matebook 14", 512, 14, 16, huawei);
		Notebook noteLenovo = new Notebook(2, 3699.0, 0.20, 10, "LENOVO V14 IGL", 1024, 14, 8, lenovo);
		Notebook noteAsus = new Notebook(3, 8199.0, 0.20, 10, "ASUS Tuf Gaming", 2048, 15.6, 32, asus);

		ArrayList<Notebook> noteBookList = new ArrayList<>();
		noteBookList.add(noteHuawei);
		noteBookList.add(noteLenovo);
		noteBookList.add(noteAsus);

		MobilePhone mobileSamsung = new MobilePhone(1, 3199.0, 0.20, 10, "SAMSUNG GALAXY A51", 512, 6.5, 4000, 6,
				samsung, "beyaz");
		MobilePhone mobileApple = new MobilePhone(2, 7379.0, 0.20, 10, "iPhone 11 64 GB", 1024, 6.1, 4000, 6, apple,
				"lacivert");
		MobilePhone mobileRedmi = new MobilePhone(3, 4012.0, 0.20, 10, "Redmi Note 10 Pro 8GB", 2048, 6.5, 4000, 12,
				xiaomi, "siyah");
		ArrayList<MobilePhone> mobilePhoneList = new ArrayList<>();
		mobilePhoneList.add(mobileSamsung);
		mobilePhoneList.add(mobileApple);
		mobilePhoneList.add(mobileRedmi);

		boolean bool = true;
		int secim;

		while (bool) {
			System.out
					.println("1 - Notebook İşlemleri\n2 - Cep Telefonu İşlemleri\n3 - Marka Listele\n0 - Çıkış Yap\n");
			System.out.print("seçiminiz: ");
			secim = scan.nextInt();
			switch (secim) {
			case 0:
				// Çıkış
				bool = false;
				break;
			case 1:
				System.out.println("1 - Notebook Ekle\n2 - Notebook Listele");
				System.out.print("seçiminiz: ");
				int noteBookCase = scan.nextInt();
				if (noteBookCase == 1) {
					noteBookList.add((Notebook) addProduct());
				} else if (noteBookCase == 2) {
					System.out.println("NoteBook Listesi");
					listNoteBook(noteBookList);

				} else {
					System.out.println("Yanlış Seçim");
				}

				break;
			case 2:
				System.out.println("1 - Cep Telefonu Ekle\n2 - Cep Telefonu Listele");
				System.out.print("seçiminiz: ");
				int mobilePhoneCase = scan.nextInt();
				if (mobilePhoneCase == 1) {
					mobilePhoneList.add((MobilePhone) addProduct());
				} else if (mobilePhoneCase == 2) {
					System.out.println("Cep Telefonu Listesi");
					listMobilePhone(mobilePhoneList);

				} else {
					System.out.println("Yanlış Seçim");
				}
				break;
			case 3:
				printBrandList(liste);
				break;

			default:
				System.out.println("Yanlış seçim");
				break;
			}
		}

	}

	private void listMobilePhone(ArrayList<MobilePhone> mobilePhoneList) {
		for (MobilePhone product : mobilePhoneList) {
			System.out.println(product.getProductName());
		}
	}

	private void listNoteBook(ArrayList<Notebook> noteBookList) {
		for (Notebook product : noteBookList) {
			System.out.println(product.getProductName());
		}
	}

	private Product addProduct() {

		System.out.println("NoteBook için Özellikleri giriniz ");
		System.out.print("Ürün adını giriniz: ");
		String productName = scan.next();
		System.out.print("id giriniz: ");
		int id = scan.nextInt();
		System.out.print("Fiyat giriniz: ");
		double price = scan.nextDouble();
		System.out.print("İndirim oranını giriniz: ");
		double discountRate = scan.nextDouble();
		System.out.print("Stok Miktarını giriniz: ");
		int stock = scan.nextInt();

		System.out.print("Depolama miktarını giriniz: ");
		int storage = scan.nextInt();
		System.out.print("Ekran boyutunu (inch) giriniz: ");
		int inch = scan.nextInt();
		System.out.print("RAM miktarını giriniz: ");
		int ram = scan.nextInt();
		Product product = null;
		if (product instanceof Notebook) {
			product = new Notebook(id, price, discountRate, stock, productName, storage, inch, ram, brandAdd());
		} else if (product instanceof MobilePhone) {
			System.out.print("Renk Giriniz: ");
			String color = scan.next();
			System.out.print("Battery Pow Giriniz: ");
			int batteryPow = scan.nextInt();
			product = new MobilePhone(id, price, discountRate, stock, productName, storage, inch, batteryPow, ram,
					brandAdd(), color);
		}

		return product;
	}

	private Brand brandAdd() {

		System.out.print("Marka id giriniz: ");
		int id = scan.nextInt();
		System.out.print("Marka adı giriniz: ");
		String name = scan.next();
		Brand brand = new Brand(id, name);
		return brand;

	}

	private void printBrandList(TreeSet<Brand> liste) {
		System.out.println("\nMarkalarımız");
		System.out.println("-----------------------");
		for (Brand brand : liste) {
			System.out.println(" - " + brand.getName());
		}
		System.out.println();

	}

}

```

## MAIN
```java

public class Main {

	public static void main(String[] args) {

		PatikaStore patikaStore = new PatikaStore();
		patikaStore.run();

	}

}

```