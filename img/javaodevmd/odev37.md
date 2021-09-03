# JAVA Odev 37 Ogrenci Bilgi Sistemi Temel Yapi

## Teacher
```Java
public class Teacher {
	String name;
	String mpno;
	String branch;

	public Teacher(String name, String mpno, String branch) {
		this.name = name;
		this.mpno = mpno;
		this.branch = branch;
	}
}

```


## Course
```java

public class Course {
	Teacher courseTeacher;
	String name;
	String code;
	String prefix;
	int note;
	int verbalNote;

	public Course(String name, String code, String prefix) {
		this.name = name;
		this.code = code;
		this.prefix = prefix;
		this.note = 0;
		this.verbalNote=0;
	}

	public void addTeacher(Teacher t) {
		if (this.prefix.equals(t.branch)) {
			this.courseTeacher = t;
			System.out.println("İşlem başarılı");
		} else {
			System.out.println(t.name + " Akademisyeni bu dersi veremez.");
		}
	}

	public void printTeacher() {
		if (courseTeacher != null) {
			System.out.println(this.name + " dersinin Akademisyeni : " + courseTeacher.name);
		} else {
			System.out.println(this.name + " dersine Akademisyen atanmamıştır.");
		}
	}
}

```


## Student
```java

public class Student {
	String name, stuNo;
	int classes;
	Course mat;
	Course fizik;
	Course kimya;
	double avarage;
	boolean isPass;

	Student(String name, int classes, String stuNo, Course mat, Course fizik, Course kimya) {
		this.name = name;
		this.classes = classes;
		this.stuNo = stuNo;
		this.mat = mat;
		this.fizik = fizik;
		this.kimya = kimya;
		calcAvarage();
		this.isPass = false;
	}

	public void addBulkExamNote(int mat, int matVerbal, int fizik, int fizikVerbal, int kimya, int kimyaVerbal) {

		if (mat >= 0 && mat <= 100) {
			this.mat.note = mat;

		}

		if (matVerbal >= 0 && matVerbal <= 100) {
			this.mat.verbalNote = matVerbal;
		}

		if (fizik >= 0 && fizik <= 100) {
			this.fizik.note = fizik;
		}

		if (fizikVerbal >= 0 && fizikVerbal <= 100) {
			this.fizik.verbalNote = fizikVerbal;
		}

		if (kimya >= 0 && kimya <= 100) {
			this.kimya.note = kimya;
		}

		if (kimyaVerbal >= 0 && kimyaVerbal <= 100) {
			this.kimya.verbalNote = kimyaVerbal;
		}

	}

	public void isPass() {
		if (this.mat.note == 0 || this.fizik.note == 0 || this.kimya.note == 0) {
			System.out.println("Notlar tam olarak girilmemiş");
		} else if (this.mat.verbalNote == 0 || this.fizik.verbalNote == 0 || this.kimya.verbalNote == 0) {
			System.out.println("Sözlü Notları tam olarak girilmemiş");
		} else {
			this.isPass = isCheckPass();
			printNote();
			System.out.println("Ortalama : " + this.avarage);
			if (this.isPass) {
				System.out.println("Sınıfı Geçti. ");
			} else {
				System.out.println("Sınıfta Kaldı.");
			}
		}
	}

	public void calcAvarage() {
		this.avarage = ((this.fizik.note * 0.80 + this.fizik.verbalNote * 0.20)
				+ (this.kimya.note * 0.80 + this.kimya.verbalNote * 0.20)
				+ (this.mat.note * 0.80 + this.mat.verbalNote * 0.20)) / 3;
	}

	public boolean isCheckPass() {
		calcAvarage();
		return this.avarage > 55;
	}

	public void printNote() {
		System.out.println("=========================");
		System.out.println("Öğrenci : " + this.name);
		System.out.println("Matematik Notu : " + this.mat.note);
		System.out.println("Matematik Sözlü Notu : " + this.mat.verbalNote);
		System.out.println("Fizik Notu : " + this.fizik.note);
		System.out.println("Fizik Sözlü Notu : " + this.fizik.verbalNote);
		System.out.println("Kimya Notu : " + this.kimya.note);
		System.out.println("Kimya Sözlü Notu : " + this.kimya.verbalNote);
	}

}

```

## MAIN
```java

public class Main {
    public static void main(String[] args) {

        Course mat = new Course("Matematik", "MAT101", "MAT");
        Course fizik = new Course("Fizik", "FZK101", "FZK");
        Course kimya = new Course("Kimya", "KMY101", "KMY");

        Teacher t1 = new Teacher("Mahmut Hoca", "90550000000", "MAT");
        Teacher t2 = new Teacher("Fatma Ayşe", "90550000001", "FZK");
        Teacher t3 = new Teacher("Ali Veli", "90550000002", "KMY");

        mat.addTeacher(t1);
        fizik.addTeacher(t2);
        kimya.addTeacher(t3);

        Student s1 = new Student("İnek Şaban", 4, "140144015", mat, fizik, kimya);
        s1.addBulkExamNote(50,50,20,40,50,60);
        s1.isPass();

        Student s2 = new Student("Güdük Necmi", 4, "2211133", mat, fizik, kimya);
        s2.addBulkExamNote(100,50,40,100,50,40);
        s2.isPass();

        Student s3 = new Student("Hayta İsmail", 4, "221121312", mat, fizik, kimya);
        s3.addBulkExamNote(50,20,40,50,20,40);
        s3.isPass();

    }
}

```

## ÇIKTI
```console
İşlem başarılı
İşlem başarılı
İşlem başarılı
=========================
Öğrenci : İnek Şaban
Matematik Notu : 50
Matematik Sözlü Notu : 50
Fizik Notu : 20
Fizik Sözlü Notu : 40
Kimya Notu : 50
Kimya Sözlü Notu : 60
Ortalama : 42.0
Sınıfta Kaldı.
=========================
Öğrenci : Güdük Necmi
Matematik Notu : 100
Matematik Sözlü Notu : 50
Fizik Notu : 40
Fizik Sözlü Notu : 100
Kimya Notu : 50
Kimya Sözlü Notu : 40
Ortalama : 63.333333333333336
Sınıfı Geçti. 
=========================
Öğrenci : Hayta İsmail
Matematik Notu : 50
Matematik Sözlü Notu : 20
Fizik Notu : 40
Fizik Sözlü Notu : 50
Kimya Notu : 20
Kimya Sözlü Notu : 40
Ortalama : 36.666666666666664
Sınıfta Kaldı.
```

