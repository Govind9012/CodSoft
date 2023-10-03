import java.util.Scanner;

public class studentGradeCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);


        System.out.print("Enter the number of subjects: ");
        int numSubjects = scanner.nextInt();

        double totalMarks = 0;
        for (int i = 1; i <= numSubjects; i++) {
            System.out.print("Enter marks obtained in subject " + i + ": ");
            double marks = scanner.nextDouble();
            totalMarks += marks;
        }


        System.out.println("Total Marks: " + totalMarks);


        double averagePercentage = totalMarks / (numSubjects * 100) * 100;
        System.out.println("Average Percentage: " + averagePercentage + "%");


        String grade;
        if (averagePercentage >= 90) {
            grade = "A+";
        } else if (averagePercentage >= 80) {
            grade = "A";
        } else if (averagePercentage >= 70) {
            grade = "B";
        } else if (averagePercentage >= 60) {
            grade = "C";
        } else if (averagePercentage >= 50) {
            grade = "D";
        } else {
            grade = "F";
        }


        System.out.println("Grade: " + grade);

        scanner.close();
    }
}
