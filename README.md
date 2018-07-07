# SumAverage
import java.util.Scanner;  // Needed for keyboard input

public class SumAverage {
   public static void main (String[] args) {
      // Declare variables
      int lowerbound, upperbound, sum = 0;
      double average;
      Scanner in = new Scanner(System.in);  // for keyboard input
      
      // Prompt and read inputs
      System.out.print("Enter the lowerbound: ");
      lowerbound = in.nextInt();
      System.out.print("Enter the upperbound: ");
      upperbound = in.nextInt();
      
      // Compute sum
      for (int number = lowerbound; number <= upperbound; ++number) {
         sum += number;
      }

      // Compute average
      // Take note that int/int gives int. Type casting needed.
      average = (double)sum/((upperbound - lowerbound) + 1);
      
      // Display results
      System.out.println("The sum is: " + sum);
      System.out.println("The average is: " + String.format("%.2f", average));
	  in.close();
   }
}
