import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.println("Практическое задание №1. Вариант 3. Студент Шалунова А.С. Группа РИБО-01-21 ");
        System.out.println("Введите начальную сумму вклада: ");
        double deposit = scan.nextDouble();
        System.out.println("Введите срок вклада (в месяцах): ");
        int month = scan.nextInt();
        System.out.println("Введите годовой процент по вкладу: ");
        double percent = scan.nextDouble();
        double monthly = percent/12;

        double income = 0;
        for (int i=1; i<=month; i++){
            income = monthly/100 * i * deposit;
            String profit = String.format("%.2f", income);
            System.out.println(i + " месяц, начисленная сумма " + profit);
        }
        deposit = deposit + income;
        System.out.println("Итоговая сумма дохода: " + deposit);
    }
}
