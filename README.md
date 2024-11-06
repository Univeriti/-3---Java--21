import java.util.Scanner;

public class FormattedOutputPractice {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Reading user input
        System.out.print("Enter an integer: ");
        int integerNumber = scanner.nextInt();

        System.out.print("Enter a floating-point number: ");
        double floatingNumber = scanner.nextDouble();

        System.out.print("Enter a string: ");
        scanner.nextLine(); // Consume newline after nextDouble()
        String text = scanner.nextLine();

        System.out.print("Enter a boolean value (true or false): ");
        boolean booleanValue = scanner.nextBoolean();

        System.out.println("\nFormatted Output:");

        // 1. Formatting with System.out.printf()
        System.out.printf("1. Integer: %d, Floating-point: %.2f, String: %s, Boolean: %b%n",
                integerNumber, floatingNumber, text, booleanValue);

        // 2. Formatting with alignment for strings and fixed precision for floating-point
        System.out.printf("2. Integer: %10d, Floating-point: %-10.3f, String: %-15s%n",
                integerNumber, floatingNumber, text);

        // 3. Formatting using different numeric systems
        System.out.printf("3. Decimal: %d, Octal: %o, Hexadecimal: %x%n",
                integerNumber, integerNumber, integerNumber);

        // 4. Formatting with different field width for strings
        System.out.printf("4. String (10 chars): %-10.10s%n", text);
        System.out.printf("4. String (15 chars, truncated): %-15.5s%n", text);

        // 5. Formatting with zero-padding for numbers
        System.out.printf("5. Number with zero-padding: %010d%n", integerNumber);

        // 6. Scientific notation for floating-point number
        System.out.printf("6. Scientific notation: %.2e%n", floatingNumber);

        // 7. Right-aligning string
        System.out.printf("7. Right-aligned string: %20s%n", text);

        // 8. Using String.format for prepared formatted text
        String formattedText = String.format("8. Prepared format: Integer: %d, Boolean: %b", integerNumber, booleanValue);
        System.out.println(formattedText);

        // 9. Using String.format with different precision
        System.out.println(String.format("9. Floating-point number with four decimal places: %.4f", floatingNumber));

        // 10. Using Formatter class for more complex formatting
        java.util.Formatter formatter = new java.util.Formatter();
        formatter.format("10. Integer: %d, Hexadecimal: %x, Octal: %o%n", integerNumber, integerNumber, integerNumber);
        System.out.print(formatter);
        formatter.close();

        scanner.close();
    }
}
