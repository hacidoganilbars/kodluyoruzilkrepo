# JAVA Odev 53 Kitap Sıralayıcı

## Book
```java


public class Book implements Comparable<Book> {

	private String name;
	private int page;
	private String author;
	private String releaseDate;

	public Book(String name, int page, String author, String releaseDate) {
		super();
		this.name = name;
		this.page = page;
		this.author = author;
		this.releaseDate = releaseDate;
	}

	// @Override
	// public int compareTo(Book o) {
	// return this.name.compareTo(o.name);
	// }

	@Override
	public int compareTo(Book o) {
		return this.page - o.page;
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

}


```

## MAIN
```java
import java.util.HashSet;
import java.util.TreeSet;

public class Main {

	public static void main(String[] args) {

		HashSet<Book> setList = new HashSet<>();
		setList.add(new Book("Cc Kitap", 100, "Özlem Koçak", "10.10.1999"));
		setList.add(new Book("Ee Kitap", 98, "Ayşe İlbars", "04.08.1991"));
		setList.add(new Book("Aa Kitap", 300, "Mustafa Çil", "01.04.2005"));
		setList.add(new Book("Dd Kitap", 150, "Tuğba Efe", "05.04.2005"));
		setList.add(new Book("Bb Kitap", 120, "Şükran Tekeli", "10.10.1999"));

		for (Book book : setList) {
			System.out.println(book.getName()+" - "+book.getPage());
		}
		
		System.out.println("----------------------------------");

		TreeSet<Book> treeSet = new TreeSet<>();
		treeSet.add(new Book("Cc Kitap", 100, "Özlem Koçak", "10.10.1999"));
		treeSet.add(new Book("Ee Kitap", 98, "Ayşe İlbars", "04.08.1991"));
		treeSet.add(new Book("Aa Kitap", 300, "Mustafa Çil", "01.04.2005"));
		treeSet.add(new Book("Dd Kitap", 150, "Tuğba Efe", "05.04.2005"));
		treeSet.add(new Book("Bb Kitap", 120, "Şükran Tekeli", "10.10.1999"));

		for (Book book : treeSet) {
			System.out.println(book.getName()+" - "+book.getPage());
		}

	}
}

```

## CONSOLE
```console
Ee Kitap
Bb Kitap
Dd Kitap
Cc Kitap
Aa Kitap
----------------------------------
Aa Kitap
Bb Kitap
Cc Kitap
Dd Kitap
Ee Kitap

```