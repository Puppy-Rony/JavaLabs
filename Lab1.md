# Отчет по лабораторной работе №1 "Поиск простых чисел. Нахождение полиндрома"
Задание 1: выести на экран все простые числа до 100. Код:
```jsx
pubic class d {
      public static void main(String[] args) {
          int n = 100;// инициализируем 100 значений
          for (int i = 2; i < n; i++) { //проходим по циклу до 100
            boolean a = true;//задаем булевое значение, при котором условие будет верным
            int q = (int) Math.sqrt(i);
            for (int j = 2; j <= q; j++) {//проходи по циклу от 2 и смотрим, делится ли наше число на кокое-либо из чисел до него
                if ((i % j) == 0) {//если делится, то это i не подходит, берем следующее, если не делится, то i - простое число 
                    a = false;
                    break;
                }
            }
            if (a) {
                System.out.println(i + " prostoe");//выводи верное условие, где i - простое
            }
        }
    }
}
```

Задание 2: определить, полиндром ли строка, вводимая пользователем, или нет. Код:
```jsx
import java.util.Scanner;
import java.util.Arrays;

public class pol {
    public static void main(String[] args) {
    	System.out.println("Enter any string ");//Просим полльзователя ввести слово - полиндром
    	Scanner in=new Scanner (System.in);// создаем переменную и используем метод Scanner, чтобы вложить в переменную строку вводимую пользователем
    	String number1= in.nextLine();//создаем переменную - строку, вводимую пользователем, через метод nextLine(), который читает до конца текущей строки (символа перевода строки или конца потока) и возвращает всё, что было в этой строке.
    	int p=0;
    	number1= number1.replace(" ","");// из строки удаляем (путем замены) пробелы
    	number1= number1.replace(",","");//запятые
    	number1= number1.replace(".","");//точки
    	char [] mass=number1.toCharArray();// создаем массив и вкладываем туда строку
    	int i=0; //создаем поинтеры начала
    	int j=mass.length-1;// и конца строки
    	for (;i<=mass.length  && j>=0; i++, j--)// проходим по циклу: от первой буквы до последней и от последней до первой 
    		if (mass[i]!=mass[j])// если первая и последняя(вторая и предпоследня и т.д) буква не равны - то не полиндром, иначе полиндром
    			p=1;
    		if (p==0)
    			System.out.println("polindrom"); else 
    		System.out.println(" NOT polindrom") ;
    }
}
```
Задание 3: объеденить две программы одним
```jsx
import java.util.Scanner;

public class Main{
	public static void main(String[] args) {
		System.out.println("Enter number to choose action ");// просим пользователя ввести число, для выбора действия
		Scanner in=new Scanner(System.in);// инициализируем метод Scanner для считывания уифры, вводимой пользователем
		int n=in.nextInt();создаем переменную - число, вводимую пользователем, через метод nextШте(), который читает до конца текущего числа (символа перевода строки или конца потока) и возвращает всё, что было в нем
		switch(n)
		{
			case 1:
				d.main(null);
				break;
			case 2:
				pol.main(null);
				break;
			default: System.out.println("NOT Correct");
		}
	}
}
```
