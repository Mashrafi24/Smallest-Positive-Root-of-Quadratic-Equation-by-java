# Smallest-Positive-Root-of-Quadratic-Equation-by-java

import java.util.Scanner;

public class Quadratic {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a: ");
        double a = sc.nextDouble();

        System.out.print("Enter b: ");
        double b = sc.nextDouble();

        System.out.print("Enter c: ");
        double c = sc.nextDouble();

        double d = b * b - 4 * a * c;

        if (d < 0) {
            System.out.println("No real roots");
        } else {
            double r1 = (-b + Math.sqrt(d)) / (2 * a);
            double r2 = (-b - Math.sqrt(d)) / (2 * a);

            double min = Double.MAX_VALUE;

            if (r1 > 0) min = r1;
            if (r2 > 0 && r2 < min) min = r2;

            if (min == Double.MAX_VALUE)
                System.out.println("No positive root");
            else
                System.out.println("Smallest positive root: " + min);
        }

        sc.close();
    }
}
