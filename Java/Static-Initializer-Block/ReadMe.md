# Problem
Static initialization blocks are executed when the class is loaded, and you can initialize static variables in those blocks.

It's time to test your knowledge of Static initialization blocks. You can read about it [here](https://docs.oracle.com/javase/tutorial/java/javaOO/initial.html).

You are given a class Solution with a main method. Complete the given code so that it outputs the area of a parallelogram with breadth  and height . You should read the variables from the standard input.

If  or  , the output should be "java.lang.Exception: Breadth and height must be positive" without quotes.

## Quick Explanations
This problem requires a static function for validation and obtaining the height value.

First, I will read two values from STDIN and pass these values to the static function.

The static function will check the validation for these values. If both are positive, 

it will return the height value. Later, we will call this function from the main method.

## Code 
```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        
        Scanner sc = new Scanner(System.in);
        int b = sc.nextInt();
        int h = sc.nextInt();
        sc.close();
        try{
            System.out.println(InitValues(b, h));
        } catch (Exception e) {
            System.out.println(e);;
        }


    }

    private static int InitValues(int b, int h) throws Exception {
        if (b <= 0 || h <= 0){
            throw new Exception("Breadth and height must be positive");
        }
        return h;
    }
}
```
