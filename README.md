# Currency Converter
import java.util.Scanner;
public class CurrencyConverter {

    public static void main(String[] args) {
        
        Scanner scanner = new Scanner(System.in);

        System.out.println("Currency Converter");
        System.out.println("1. USD to EUR");
        System.out.println("2. USD to GBP");
        System.out.println("3. EUR to USD");
        System.out.println("4. EUR to GBP");
        System.out.print("Choose a conversion (1-4): ");
        int choice = scanner.nextInt();

        
        System.out.print("Enter the amount you want to convert: ");
        double amount = scanner.nextDouble();

        
        double usdToEur = 0.85;
        double usdToGbp = 0.75;
        double eurToUsd = 1.18;
        double eurToGbp = 0.88;

    
        double result = 0;
        String currency = "";
        
        switch (choice) {
            case 1:
                result = amount * usdToEur;
                currency = "EUR";
                break;
            case 2:
                result = amount * usdToGbp;
                currency = "GBP";
                break;
            case 3:
                result = amount * eurToUsd;
                currency = "USD";
                break;
            case 4:
                result = amount * eurToGbp;
                currency = "GBP";
                break;
            default:
                System.out.println("Invalid choice!");
                return;
        }

        
        System.out.printf("Converted amount: %.2f %s%n", result, currency);
    }
}
