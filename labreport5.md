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

Student Reply:
Here is how my code looks like now
```
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] myArray = {4, -2, 8, %, 5, 12}; 
        System.out.println(Arrays.toString(myArray));
        double average = calculateAverage(myArray);
        System.out.println("Average: " + average);
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
My code is outputting weird stuff

Staff Response:
Try compiling and running the file in the terminal and then run calculateAverage.sh to only run the average function.

Student Response:
```
$ ./calculateAverage.sh

[4, -2, 8, %, 5, 12]
Exception in thread "main" java.util.InputMismatchException
    at java.base/java.util.Scanner.throwFor(Scanner.java:939)
    at java.base/java.util.Scanner.next(Scanner.java:1594)
    at java.base/java.util.Scanner.nextInt(Scanner.java:2258)
    at java.base/java.util.Scanner.nextInt(Scanner.java:2212)
    at Main.main(Main.java:8)

```
This is what is outputted when I typed that in


Staff Reponse:
Thank you for the screenshot is seems the reason for this error is due to the special character "%" being in the array as your code can't handle that value in the array which results in the calculateAverage function not working properly, to fix this replace this with an acutal numerical value and you should be good to go, you can make further modifications to you code so that it can handle characters that aren't integer values. 















Reflection Part 2:
The coolest thing that I learned in the second half for this class was learning how to use vim text editor in lab. Up until now I always thought the only way to edit code was thorugh some type of development environment like intellj, vsCode, etc. When I found out about vim, I was happy to learn that there was a way to save so much time as you could edit code and fix mistakes without having to fully load up one of those environments which is usally a pain. It was also pretty fun to learn all of the commands for vim like how x is to delete a character or you type i to start inserting characters and much more. Learning how to use vim was a nice change in pace for the class as I found the previous week to be boring. I think part of the reason why I found the lab so fun was that it encouraged us to get faster and better with vim at our own pace rather than rush us to accomplish one task or fix a mistake like some of the other prior labs. Overall, I think learning vim was one of the most fun and memorable parts of the class.  
