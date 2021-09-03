# JAVA Odev 39 Maaş Hesaplayıcı

## Emplooye
```java
public class Employee {

	String name;
	double salary;
	int workHours;
	int hireYear;

	public Employee(String name, double salary, int workHours, int hireYear) {
		this.name = name;
		this.salary = salary;
		this.workHours = workHours;
		this.hireYear = hireYear;
	}

	double tax() {
		double taxMiktari = 0;
		if (this.salary > 1000) {
			taxMiktari = this.salary * 0.03;
		}
		return taxMiktari;
	}

	double bonus() {
		int time;
		double bonus = 0;
		if (workHours > 40) {
			time = workHours - 40;
			bonus = 30 * time;
		}
		return bonus;
	}

	double raiseSalary() {
		double realSalary = 0;
		int extraYear = 2021-hireYear;
		if (extraYear < 10) {
			realSalary = salary * 0.05;
		} else if (extraYear > 9 && hireYear < 20) {
			realSalary = salary * 0.10;
		} else if (extraYear > 19) {
			realSalary = salary * 0.15;
		}
		return realSalary;
	}

	//Toplam maaşa neden bonus ve vergiyi eklemedik bilmiyorum :D
	public String toString() {
		double toplamMaas = this.salary+this.raiseSalary();
		double vergiBonus= this.salary+this.bonus()-this.tax();
		
		return "Adı : "+ this.name+
				"\nMaaşı : "+this.salary+
				"\nÇalışma Saati : "+this.workHours+
				"\nBaşlangıç Yılı : "+ this.hireYear+
				"\nVergi : "+this.tax()+
				"\nBonus : "+this.bonus()+
				"\nMaaş Artışı : "+ (toplamMaas-this.salary)+
				"\nVergi ve Bonuslar ile birlikte maaş : " +vergiBonus+
				"\nToplam Maaş : "+toplamMaas;
	}
}


```

## MAIN
```java
public class Main {

	public static void main(String[] args) {
		Employee employee = new Employee("Kemal", 2000.0, 45, 1985);
		String kemal = employee.toString();
		System.out.println(kemal);
	}
}

```

## Console
```console
Adı : Kemal
Maaşı : 2000.0
Çalışma Saati : 45
Başlangıç Yılı : 1985
Vergi : 60.0
Bonus : 150.0
Maaş Artışı : 300.0
Vergi ve Bonuslar ile birlikte maaş : 2090.0
Toplam Maaş : 2300.0

```