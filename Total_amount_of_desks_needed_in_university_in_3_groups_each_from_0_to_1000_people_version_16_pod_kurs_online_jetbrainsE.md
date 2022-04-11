# Java---programy-dzialajace

/*
 This program is checking how many desks will be need in university:

 On 3 groups.
 On every group there is from 0 to 1000 students.

 In situation that number of desks is odd then
 person who seats without another student in front of that
 desk also have desk.

|-------------------------------------------
|1. example:                                |
| enter number of people in first group:    |
| 100                                       |
| enter number of people in second group:   |
| 50                                        |
| enter number of people in third group:    |
| 41                                        |
|                                           |
| Total amount of desks in 3 groups: 96     |
--------------------------------------------|

|-------------------------------------------
| 2. example:                               |
| enter number of people in first group:    |
| 20                                        |
| enter number of people in second group:   |
| 21                                        |
| enter number of people in third group:    |
| 22                                        |
|                                           |
| Total amount of desks in 3 groups: 32     |
--------------------------------------------|

|-------------------------------------------
| 3. example:                               |
| enter number of people in first group:    |
| 16                                        |
| enter number of people in second group:   |
| 18                                        |
| enter number of people in third group:    |
| 20                                        |
|                                           |
|Total amount of desks in 3 groups: 27      |
--------------------------------------------|
*/


package nauka_z_hyperskill;
import java.util.Scanner;

public class Total_amount_of_desks_needed_in_university_in_3_groups_each_from_0_to_1000_people_version_16_pod_kurs_online_jetbrains {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int enteredNumber = 0;
        int amountDesksInOneGroup = 0;
        int firstGroup = 0;
        int secondGroup = 0;
        int thirdGroup = 0;

        // Precised amount of grups of studens in university.
        for ( int a = 1; a<=3; a++){

         int group = 0;
         int TotalAmountOfDesks = 0;

         System.out.println("Enter the number of people in the group " +a+ ":");

         if (a == 1 ){
                System.out.println("First click mouse button below this line to be able enter value.");
            }

            enteredNumber = scanner.nextInt();

         while ((enteredNumber < 0) || (enteredNumber > 1000)) {

             System.out.println("Enter value from 0 to 1000 which " +
                     " accurate number of people in " + a + " group ");
             enteredNumber = scanner.nextInt();
         }

         if ((enteredNumber % 2) == (0)) {
             amountDesksInOneGroup = enteredNumber / 2;
             group = amountDesksInOneGroup;
         } else if ((enteredNumber % 2) != (0)) {
             amountDesksInOneGroup = (enteredNumber + 1) / 2;
             group = amountDesksInOneGroup;
         }

         if (a == 1){
             firstGroup = group;
         }
         if (a == 2){
             secondGroup = group;
         }
         if (a == 3){
             thirdGroup = group;
         }

         if (a == 3){
             TotalAmountOfDesks = firstGroup+secondGroup+thirdGroup;
         }
         if (a == 3){
             System.out.println(""); // this line for better visibility of examples
             System.out.print("Total amount of desks in 3 groups: ");
             System.out.println(TotalAmountOfDesks);
            }

       }
    }
}




