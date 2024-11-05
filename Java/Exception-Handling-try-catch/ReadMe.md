# Problem
Exception handling is the process of responding to the occurrence, during computation, of exceptions – anomalous or exceptional conditions requiring special processing – often changing the normal flow of program execution. (Wikipedia)

Java has built-in mechanism to handle exceptions. Using the try statement we can test a block of code for errors. The catch block contains the code that says what to do if exception occurs.

This problem will test your knowledge on try-catch block.

You will be given two integers  and  as input, you have to compute . If  and  are not  bit signed integers or if  is zero, exception will occur and you have to report it. Read sample Input/Output to know what to report in case of exceptions.
## Code
```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner in = new Scanner(System.in);

        try {
            int x = in.nextInt();
            int y = in.nextInt();
            try{
                int a = x / y;
                System.out.println(a);
            }catch (Exception e){
                System.out.println(e);
            }
        } catch (InputMismatchException e) {
            System.out.println(e.getClass().getName());
        }

        in.close();
    }
}
```
