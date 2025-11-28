Java Calculator

A simple console-based calculator written in Java that performs basic arithmetic operations such as Addition, Subtraction, Multiplication, and Division.
This program uses Java’s "Scanner" class to take user input and a "switch" statement to process operations.

---

📌 Features

- Addition ("+")
- Subtraction ("-")
- Multiplication ("*")
- Division ("/") with zero-division handling
- Clean and easy-to-understand structure

---

🧩 How It Works

1. The program asks the user to input two numbers.
2. The user selects an operation by entering a number (1–4).
3. The calculator performs the chosen operation and displays the result.
4. Division includes an error check for division by zero.

---

▶️ Running the Program

1. Compile

javac Calculator.java

2. Run

java Calculator

---

📄 Code Example

import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("----- Simple Calculator -----");
        System.out.print("Enter first number: ");
        double num1 = sc.nextDouble();

        System.out.print("Enter second number: ");
        double num2 = sc.nextDouble();

        System.out.println("Choose an operation:");
        System.out.println("1. Addition (+)");
        System.out.println("2. Subtraction (-)");
        System.out.println("3. Multiplication (*)");
        System.out.println("4. Division (/)");
        System.out.print("Enter choice: ");
        int choice = sc.nextInt();

        double result;

        switch (choice) {
            case 1:
                result = num1 + num2;
                System.out.println("Result = " + result);
                break;

            case 2:
                result = num1 - num2;
                System.out.println("Result = " + result);
                break;

            case 3:
                result = num1 * num2;
                System.out.println("Result = " + result);
                break;

            case 4:
                if (num2 != 0) {
                    result = num1 / num2;
                    System.out.println("Result = " + result);
                } else {
                    System.out.println("Error: Cannot divide by zero!");
                }
                break;

            default:
                System.out.println("Invalid choice!");
        }

        sc.close();
    }
}

---

🛠 Requirements

- Java Development Kit (JDK) 8 or above

---

📌 Future Enhancements (Optional)

- Add scientific functions (sin, cos, sqrt, power)
- GUI version using Java Swing
- Object-Oriented calculator
- Error-proof input validation

---

📜 License

This project is free to use and modify.

---
