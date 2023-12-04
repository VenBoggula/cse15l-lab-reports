Student Post:
Issue with Calculations in Java Program

Hello,
I'm currently working on a Java program for my class project, and I've run into a strange issue. I've attached a screenshot below that shows the problem. The program is supposed to calculate the average of an array of numbers, but it seems like the result is way off. I've double-checked my code, and I can't figure out what's going wrong. Any help would be greatly appreciated!

Here is a screenshot of my file
```
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] myArray = {4, -2, 8, %, 5, 12};
        double average = calculateAverage(myArray);
    }

    public static double calculateAverage(int[] array) {
        int sum = 0;
        for (int num : array) {
            sum += num;
        }
        return (double) sum / array.length;
    }
}
```
Staff Response:
Maybe you could you try printing out the values in your array before you calculate the average? It might help both of us to understand what's going wrong. You can use the System.out.println(Arrays.toString(yourArray)); statement each calculation to see where exactly the mistake is.


