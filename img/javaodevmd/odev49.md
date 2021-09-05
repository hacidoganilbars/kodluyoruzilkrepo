## JAVA Odev 49 Mayın Tarlası

```java
import java.util.Random;
import java.util.Scanner;

public class MineSweeper {
	Scanner sc = new Scanner(System.in);
	int row;
	int column;
	String arr[][];
	int bombaSayisi;

	public MineSweeper() {

	}

	public MineSweeper(int row, int column) {
		this.row = row;
		this.column = column;
	}

	public void run() {
		System.out.print("Satır Sayısını Giriniz : ");
		row = sc.nextInt();
		System.out.print("Sütun Sayısını Giriniz : ");
		column = sc.nextInt();
		bombaSayisi = (this.row * this.column) / 4;
		tarlaOlustur(bombaSayisi);
	}

	public void tarlaOlustur(int bombaSayisi) {
		arr = new String[this.row][this.column];
		int[] rndArr;
		for (int i = 0; i < row; i++) {
			for (int j = 0; j < this.column; j++) {
				arr[i][j] = "-";
			}
		}
		for (int i = 0; i < bombaSayisi; i++) {
			do {
				rndArr = mayin();

			} while (arr[rndArr[0]][rndArr[1]].equals("*"));
			arr[rndArr[0]][rndArr[1]] = "*";
		}

		System.out.println("Mayınların Konumu");

		for (int i = 0; i < this.row; i++) {
			for (int j = 0; j < this.column; j++) {
				System.out.print(arr[i][j] + " ");
			}
			System.out.print("\n");
		}
		cizgi();
		oyna(arr);

	}

	public int[] mayin() {
		Random rnd = new Random();
		int[] mayinKonum = { rnd.nextInt(this.row), rnd.nextInt(this.column) };
		return mayinKonum;
	}

	public void cizgi() {
		System.out.println("==========================");
	}

	public void oyna(String[][] matrix) {
		System.out.println("Mayın Tarlası Oyununa Hoş Geldiniz !");
		String[][] gizliMatrix = new String[this.row][this.column];
		for (int i = 0; i < this.row; i++) {
			for (int j = 0; j < this.column; j++) {
				gizliMatrix[i][j] = "-";
			}
		}
		boolean status = true;
		int count = 0;
		int r, c, info = 0;
		do {
			for (int i = 0; i < this.row; i++) {
				for (int j = 0; j < this.column; j++) {
					System.out.print(gizliMatrix[i][j] + " ");
				}
				System.out.print("\n");
			}
			do {
				System.out.print("Satır Giriniz : ");
				r = sc.nextInt();
				System.out.print("Sutun Giriniz : ");
				c = sc.nextInt();
				if (r >= this.row || c >= this.column) {
					System.out.println("Satır veya sutun sayısından buyuk sayı girmeyiniz. Lütfen Tekrar Deneyin. ");
				}
			} while (r >= this.row || c >= this.column);

			if (matrix[r][c].equals("*")) {
				System.out.println("Game Over!!");
				status = false;
			} else {
				info = 0;
				if (r - 1 >= 0) {
					if (matrix[r - 1][c].equals("*")) {
						info++;
					}
				}
				if (r - 1 >= 0 && c - 1 >= 0) {
					if (matrix[r - 1][c - 1].equals("*")) {
						info++;
					}
				}
				if (c - 1 >= 0) {
					if (matrix[r][c - 1].equals("*")) {
						info++;
					}
				}
				if (c + 1 < this.column) {
					if (matrix[r][c + 1].equals("*")) {
						info++;
					}
				}
				if (c + 1 < this.column && r + 1 < this.row) {
					if (matrix[r + 1][c + 1].equals("*")) {
						info++;
					}
				}
				if (r + 1 < this.row) {
					if (matrix[r + 1][c].equals("*")) {
						info++;
					}
				}
				if (r - 1 >= 0 && c + 1 < this.column) {
					if (matrix[r - 1][c + 1].equals("*")) {
						info++;
					}
				}
				if (r + 1 < this.row && c - 1 >= 0) {
					if (matrix[r + 1][c - 1].equals("*")) {
						info++;
					}
				}
				gizliMatrix[r][c] = String.valueOf(info);
				count++;
			}
			cizgi();
		} while (status && count < (row * column) - ((row * column) / 4));
		if (status) {
			System.out.println("Oyunu Kazandınız !");
			for (int i = 0; i < row; i++) {
				for (int j = 0; j < column; j++) {
					if (gizliMatrix[i][j].equals("-")) {
						System.out.print("* ");
					} else {
						System.out.print(gizliMatrix[i][j] + " ");
					}
				}
				System.out.print("\n");
			}
		}
	}
}

```