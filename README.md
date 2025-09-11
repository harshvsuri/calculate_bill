# calculate_bill
program to calculate bill
import java.util.Scanner;

public class ElectricityBill {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        
        System.out.print("Enter units consumed: ");
        int units = sc.nextInt();

        double bill = 0;

        
        if (units <= 100) {
            bill = units * 1.5;
        } else if (units <= 200) {
            bill = 100 * 1.5 + (units - 100) * 3;
        } else if (units <= 300) {
            bill = 100 * 1.5 + 100 * 3 + (units - 200) * 4.5;
        } else {
            bill = 100 * 1.5 + 100 * 3 + 100 * 4.5 + (units - 300) * 6;
        }

    
        System.out.println("Total bill = Rs. " + bill);

    }
}
