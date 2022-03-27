# Check-leap-year-in-java
Check leap year in java
import java.util.Scanner;
public class NamNhuan {
    public static void main(String[] args) {
        int year;
        Scanner scan = new Scanner(System.in);
        System.out.println("Enter the year you want to check:");
        year = scan.nextInt();
        scan.close();
        boolean isLeap = false;
        if(year % 4 == 0)//divisible by 4 is a leap year
        {
            if( year % 100 == 0)
            //if it's divisible by 4 but also divisible by 100, it's not a leap year
            {
                if ( year % 400 == 0)//divisible by 400 is a leap year
                    isLeap = true;
                else
                    isLeap = false; // If it is not divisible by 400, it is not a leap year
            }
            else//divisible by 4 but not divisible by 100 is a leap year
                isLeap = true;
        }
        else {
            isLeap = false;
        }
        if(isLeap==true)
            System.out.println(year + " is a leap year.");
        else
            System.out.println(year + " is not a leap year.");
    }
}
