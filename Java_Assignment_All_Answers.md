# SWE3311 Java Programming Assignment
Student: [Your Name]

---

## Question 1: Student Grading System (if / else if)

```java
import java.util.Scanner;

public class Question1_StudentGrading {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter student's score: ");
        int score = input.nextInt();

        if (score < 0 || score > 100) {
            System.out.println("Error: Score must be between 0 and 100.");
        } else if (score >= 70 && score <= 100) {
            System.out.println("Grade: A");
        } else if (score >= 60 && score <= 69) {
            System.out.println("Grade: B");
        } else if (score >= 50 && score <= 59) {
            System.out.println("Grade: C");
        } else if (score >= 45 && score <= 49) {
            System.out.println("Grade: D");
        } else if (score >= 40 && score <= 44) {
            System.out.println("Grade: E");
        } else {
            System.out.println("Error: Score does not fall under any grade (Fail).");
        }

        input.close();
    }
}
```

---

## Question 2: Lab Allocation (switch statement)

```java
import java.util.Scanner;

public class Question2_LabAllocation {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Enter the last digit of your registration number: ");
        int digit = input.nextInt();

        switch (digit) {
            case 0:
            case 2:
            case 4:
            case 6:
            case 8:
                System.out.println("You have been assigned to Lab 4.");
                break;
            case 1:
            case 3:
            case 5:
            case 7:
            case 9:
                System.out.println("You have been assigned to Lab 3.");
                break;
            default:
                System.out.println("Invalid digit entered. Please enter a single digit (0-9).");
        }

        input.close();
    }
}
```

---

## Question 3: Discount Policy (do...while + if...else)

```java
import java.util.Scanner;

public class Question3_DiscountPolicy {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int choice;

        do {
            System.out.println("\n----- ABSAD Company Discount Menu -----");
            System.out.println("1. Individual Customer");
            System.out.println("2. Retailer");
            System.out.println("3. Exit");
            System.out.print("Select an option: ");
            choice = input.nextInt();

            if (choice == 1) {
                System.out.print("Enter number of packets ordered: ");
                int quantity = input.nextInt();
                double discount;

                if (quantity >= 12) {
                    discount = 30;
                } else {
                    discount = 0;
                }

                System.out.println("Individual Customer Discount: " + discount + "%");

            } else if (choice == 2) {
                System.out.print("Enter number of packets ordered: ");
                int quantity = input.nextInt();
                double discount;

                if (quantity < 12) {
                    discount = 15;
                } else if (quantity >= 13 && quantity <= 48) {
                    discount = 30;
                } else if (quantity > 48 && quantity <= 84) {
                    discount = 40;
                } else if (quantity >= 85) {
                    discount = 50;
                } else {
                    discount = 0;
                }

                System.out.println("Retailer Discount: " + discount + "%");

            } else if (choice == 3) {
                System.out.println("Exiting program. Goodbye!");
            } else {
                System.out.println("Invalid option. Please select 1, 2, or 3.");
            }

        } while (choice != 3);

        input.close();
    }
}
```

---

## Question 4: Compare Two Numbers (do...while)

```java
import java.util.Scanner;

public class Question4_CompareNumbers {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        char again;

        do {
            System.out.print("Enter first number: ");
            double num1 = input.nextDouble();

            System.out.print("Enter second number: ");
            double num2 = input.nextDouble();

            if (num1 == num2) {
                System.out.println("NUMBERS ARE EQUAL");
            } else {
                System.out.println("NUMBERS ARE NOT EQUAL");
                if (num1 > num2) {
                    System.out.println("FIRST NUMBER BIGGER");
                } else {
                    System.out.println("SECOND NUMBER BIGGER");
                }
            }

            System.out.print("Do you want to enter another pair of numbers? (y/n): ");
            again = input.next().charAt(0);

        } while (again == 'y' || again == 'Y');

        System.out.println("Program ended.");
        input.close();
    }
}
```
