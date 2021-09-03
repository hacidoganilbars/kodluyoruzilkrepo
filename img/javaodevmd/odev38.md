# JAVA Odev 38 Random Boks Maci

## Fighter
```java
public class Fighter {
	String name;
	int damage;
	int health;
	int weight;
	double dodge;

	public Fighter(String name, int damage, int health, int weight, double dodge) {
		this.name = name;
		this.damage = damage;
		this.health = health;
		this.weight = weight;
		this.dodge = dodge;

	}

	public int hit(Fighter foe) {

		System.out.println("------------");
		System.out.println(this.name + " => " + foe.name + " " + this.damage + " hasar vurdu.");

		if (foe.dodge()) {
			System.out.println(foe.name + " gelen hasarı savurdu.");
			return foe.health;
		}

		if (foe.health - this.damage < 0)
			return 0;

		return foe.health - this.damage;
	}

	

	public boolean dodge() {
		double randomValue = Math.random() * 100; // 0.0 to 99.9
		return randomValue <= this.dodge;
	}

}

```

## Ring
```java
public class Ring {
	Fighter f1;
	Fighter f2;
	int minWeight;
	int maxWeight;

	public Ring(Fighter f1, Fighter f2, int minWeight, int maxWeight) {
		this.f1 = f1;
		this.f2 = f2;
		this.minWeight = minWeight;
		this.maxWeight = maxWeight;
	}

	public void run() {

		if (checkWeight()) {
			while (f1.health > 0 && f2.health > 0) {
				System.out.println("======== YENİ ROUND ===========");
				f2.health = f1.hit(f2);
				if (isWin()) {
					break;
				}
				f1.health = f2.hit(f1);
				if (isWin()) {
					break;
				}
				printScore();
			}

		} else {
			System.out.println("Sporcuların ağırlıkları uyuşmuyor.");
		}

	}

	public boolean checkWeight() {
		return (f1.weight >= minWeight && f1.weight <= maxWeight) && (f2.weight >= minWeight && f2.weight <= maxWeight);
	}

	public boolean isWin() {
		if (f1.health == 0) {
			System.out.println("Maçı Kazanan : " + f2.name);
			return true;
		}
		if (f2.health == 0) {
			System.out.println("Maçı Kazanan : " + f1.name);
			return true;
		}

		return false;
	}

	boolean firstAttack(Fighter f1, Fighter f2) {

		int randomValue = (int) ((Math.random() * 2) + 1);
		if (randomValue == 1) {
			f1.hit(f2);
			return true;
			
		} else if (randomValue == 2) {
			f2.hit(f1);
			return true;
		}
		return false;
	}

	public void printScore() {
		System.out.println("------------");
		System.out.println(f1.name + " Kalan Can \t:" + f1.health);
		System.out.println(f2.name + " Kalan Can \t:" + f2.health);
	}
}


```

## MAIN
```java
public class Main {
	public static void main(String[] args) {
		Fighter marc = new Fighter("Marc", 15, 100, 100, 0);
		Fighter alex = new Fighter("Alex", 20, 100, 100, 0);
		Ring r = new Ring(marc, alex, 90, 100);
		r.firstAttack(marc, alex);
		r.run();

	}
}

```

## Console
```console
------------
Marc => Alex 15 hasar vurdu.
======== YENİ ROUND ===========
------------
Marc => Alex 15 hasar vurdu.
------------
Alex => Marc 20 hasar vurdu.
------------
Marc Kalan Can 	:80
Alex Kalan Can 	:85
======== YENİ ROUND ===========
------------
Marc => Alex 15 hasar vurdu.
------------
Alex => Marc 20 hasar vurdu.
------------
Marc Kalan Can 	:60
Alex Kalan Can 	:70
======== YENİ ROUND ===========
------------
Marc => Alex 15 hasar vurdu.
------------
Alex => Marc 20 hasar vurdu.
------------
Marc Kalan Can 	:40
Alex Kalan Can 	:55
======== YENİ ROUND ===========
------------
Marc => Alex 15 hasar vurdu.
------------
Alex => Marc 20 hasar vurdu.
------------
Marc Kalan Can 	:20
Alex Kalan Can 	:40
======== YENİ ROUND ===========
------------
Marc => Alex 15 hasar vurdu.
------------
Alex => Marc 20 hasar vurdu.
Maçı Kazanan : Alex

```