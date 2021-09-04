# JAVA Odev 46 Matrisin Transpozu

## MatrisinTranspozu

```java
import java.util.Arrays;

public class MatrisinTranspozu {

	public static void main(String[] args) {
		int[][] matrix = { { 2, 3, 4 }, { 5, 6, 4 } };
		int[][] transposed = getTranspoze(matrix);

		System.out.println("Matris: ");
		printMatrix(matrix);
		System.out.println("Transpoze: ");
		printMatrix(transposed);

	}

	static int[][] getTranspoze(int[][] matrix) {

		int length1 = matrix.length;
		int length2 = matrix[0].length;
		int[][] transpozed = new int[length2][length1];

		for (int i = 0; i < transpozed.length; i++) {
			for (int j = 0; j < transpozed[i].length; j++) {
				transpozed[i][j] = matrix[j][i];
			}
		}

		return transpozed;
	}

	static void printMatrix(int[][] matrix) {
		for (int i = 0; i < matrix.length; i++) {
			for (int j = 0; j < matrix[i].length; j++) {
				System.out.print(matrix[i][j] + "   ");
			}
			System.out.println("\n");
		}
	}
}

```

## Console
```console
Matris: 
2   3   4   

5   6   4   

Transpoze: 
2   5   

3   6   

4   4   

```