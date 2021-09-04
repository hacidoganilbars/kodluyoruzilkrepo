# JAVA Odev 42 Cok Boyutlu Array Kullanarak Yıldızlarla B Harfi Çizme

## YildizlarlaBHarfiCokBoyutluArrayle

```java

public class YildizlarlaBHarfiCokBoyutluArrayle {

	public static void main(String[] args) {
		String[][] letter = new String[7][5];

		for (int i = 0; i < letter.length; i++) {
			for (int j = 0; j < letter[i].length; j++) {

				if (i == 0 || i == 3 || i == 6) {
					letter[i][j] = " * ";
				} else if (j == 0 || j == 4) {
					letter[i][j] = " * ";
				} else {
					letter[i][j] = "   ";
				}
			}
		}

		System.out.println();
		for (String[] row : letter) {
			System.out.println();
			for (String col : row) {
				System.out.print(col);
			}
			System.out.println();
		}

	}

}

```

## Console
```console


 *  *  *  *  * 

 *           * 

 *           * 

 *  *  *  *  * 

 *           * 

 *           * 

 *  *  *  *  * 

 ```