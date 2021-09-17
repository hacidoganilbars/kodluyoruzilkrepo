# JAVA Odev 55 Kitap Listesi Stream Lambda

## Book
```java

public class Book {

	private String name;
	private int page;
	private String author;
	private String releaseDate;

	public Book(String name, int page, String author, String releaseDate) {
		this.name = name;
		this.page = page;
		this.author = author;
		this.releaseDate = releaseDate;
	}

	public String getName() {
		return name;
	}

	public void setName(String name) {
		this.name = name;
	}

	public int getPage() {
		return page;
	}

	public void setPage(int page) {
		this.page = page;
	}

	public String getAuthor() {
		return author;
	}

	public void setAuthor(String author) {
		this.author = author;
	}

	public String getReleaseDate() {
		return releaseDate;
	}

	public void setReleaseDate(String releaseDate) {
		this.releaseDate = releaseDate;
	}

	@Override
	public String toString() {
		// TODO Auto-generated method stub
		return "Kitap Adı: " + this.getName() + " Sayfa Sayısı: " + this.getPage() + " Yazarı: " + this.getAuthor()
				+ " Yayın Tarihi: " + this.getReleaseDate();
	}

}

```

## MAIN
```java
import java.util.ArrayList;

public class Main {

	public static void main(String[] args) {
		Book book1 = new Book("Aa kitap", 150, "Özlem", "16.04.1987");
		Book book2 = new Book("Bb kitap", 40, "Hacı", "16.04.1987");
		Book book3 = new Book("Cc kitap", 250, "Doğan", "16.04.1987");
		Book book4 = new Book("Dd kitap", 100, "Ayşe", "16.04.1987");
		Book book5 = new Book("Ee kitap", 15, "İsmail", "16.04.1987");
		Book book6 = new Book("Ff kitap", 300, "Eda", "16.04.1987");
		Book book7 = new Book("Gg kitap", 60, "Figen", "16.04.1987");
		Book book8 = new Book("Hh kitap", 100, "Mahmut", "16.04.1987");
		Book book9 = new Book("Jj kitap", 325, "Zekiye", "16.04.1987");
		Book book10 = new Book("Zz kitap", 800, "Selami", "16.04.1987");

		ArrayList<Book> kitapBilgiler = new ArrayList<>();

		kitapBilgiler.add(book1);
		kitapBilgiler.add(book2);
		kitapBilgiler.add(book3);
		kitapBilgiler.add(book4);
		kitapBilgiler.add(book5);
		kitapBilgiler.add(book6);
		kitapBilgiler.add(book7);
		kitapBilgiler.add(book8);
		kitapBilgiler.add(book9);
		kitapBilgiler.add(book10);

		kitapBilgiler.stream().map(book -> book.getName() + " " + book.getAuthor())
				.forEach(book -> System.out.println(book));

		System.out.println("####################");
		kitapBilgiler.stream().filter(book -> book.getPage() > 100).forEach(book -> System.out.println(book));

	}

}

```

## CONSOLE
```console
Aa kitap Özlem
Bb kitap Hacı
Cc kitap Doğan
Dd kitap Ayşe
Ee kitap İsmail
Ff kitap Eda
Gg kitap Figen
Hh kitap Mahmut
Jj kitap Zekiye
Zz kitap Selami
####################
Kitap Adı: Aa kitap Sayfa Sayısı: 150 Yazarı: Özlem Yayın Tarihi: 16.04.1987
Kitap Adı: Cc kitap Sayfa Sayısı: 250 Yazarı: Doğan Yayın Tarihi: 16.04.1987
Kitap Adı: Ff kitap Sayfa Sayısı: 300 Yazarı: Eda Yayın Tarihi: 16.04.1987
Kitap Adı: Jj kitap Sayfa Sayısı: 325 Yazarı: Zekiye Yayın Tarihi: 16.04.1987
Kitap Adı: Zz kitap Sayfa Sayısı: 800 Yazarı: Selami Yayın Tarihi: 16.04.1987

```