# java
import java.util.Scanner;

public class Main {
    private static String simulatedFile = ""; // Simulated file content

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int choice;

        do {
            System.out.println("\nSimulated File Handling Utility (Online Compiler Version)");
            System.out.println("1. Write to File");
            System.out.println("2. Append to File");
            System.out.println("3. Read File");
            System.out.println("4. Clear File");
            System.out.println("5. Exit");
            System.out.print("Enter your choice: ");
            choice = scanner.nextInt();
            scanner.nextLine();  // consume newline

            switch (choice) {
                case 1:
                    System.out.print("Enter text to write: ");
                    simulatedFile = scanner.nextLine();
                    System.out.println("Simulated file written.");
                    break;
                case 2:
                    System.out.print("Enter text to append: ");
                    simulatedFile += "\n" + scanner.nextLine();
                    System.out.println("Text appended.");
                    break;
                case 3:
                    System.out.println("\n--- File Content ---");
                    System.out.println(simulatedFile.isEmpty() ? "(File is empty)" : simulatedFile);
                    break;
                case 4:
                    simulatedFile = "";
                    System.out.println("Simulated file cleared.");
                    break;
                case 5:
                    System.out.println("Exiting...");
                    break;
                default:
                    System.out.println("Invalid choice.");
            }
        } while (choice != 5);

        scanner.close();
    }
}
