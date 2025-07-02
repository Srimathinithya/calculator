import java.util.Scanner;

public class calculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double a, b, result;
        int choice;

        do {
            System.out.println("\nSimple Calculator");
            System.out.println("1. Add");
            System.out.println("2. Subtract");
            System.out.println("3. Multiply");
            System.out.println("4. Divide");
            System.out.println("5. Exit");
            System.out.print("Enter your choice: ");
            choice = sc.nextInt();

            if (choice >= 1 && choice <= 4) {
                System.out.print("Enter first number: ");
                a = sc.nextDouble();
                System.out.print("Enter second number: ");
                b = sc.nextDouble();

                switch (choice) {
                    case 1:
                        result = a + b;
                        System.out.printf("Result: %.2f\n", result);
                        break;
                    case 2:
                        result = a - b;
                        System.out.printf("Result: %.2f\n", result);
                        break;
                    case 3:
                        result = a * b;
                        System.out.printf("Result: %.2f\n", result);
                        break;
                    case 4:
                        if (b != 0) {
                            result = a / b;
                            System.out.printf("Result: %.2f\n", result);
                        } else {
                            System.out.println("Error: Division by zero!");
                        }
                        break;
                }
            } else if (choice != 5) {
                System.out.println("Invalid choice, please try again.");
            }
        } while (choice != 5);

        System.out.println("Calculator closed. Goodbye!");
        sc.close();
    }
}
