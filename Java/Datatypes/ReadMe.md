# Problem
Java has 8 primitive data types; char, boolean, byte, short, int, long, float, and double. For this exercise, we'll work with the primitives used to hold integer values (byte, short, int, and long):

A byte is an 8-bit signed integer.
A short is a 16-bit signed integer.
An int is a 32-bit signed integer.
A long is a 64-bit signed integer.
Given an input integer, you must determine which primitive data types are capable of properly storing that input.

To get you started, a portion of the solution is provided for you in the editor.

## Solution
I used the math lib for the accounting pows. You can read from reference link, witch data types is fitting in the witch value.
Reference: https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html


### Code
```java
import java.util.*;
import java.io.*;



class Solution{
    public static void main(String []argh)
    {

        

        Scanner sc = new Scanner(System.in);
        int t=sc.nextInt();

        for(int i=0;i<t;i++)
        {

            try
            {
                long x=sc.nextLong();
                System.out.println(x+" can be fitted in:");
                if(x>=-128 && x<=127){
                    System.out.println("* byte");
                }
                if(x>=-Math.pow(2,15) && x<=Math.pow(2,15)-1){
                    System.out.println("* short");
                }
                if(x>=-Math.pow(2,31) && x<=Math.pow(2,31)-1){
                    System.out.println("* int");
                }
                if(x>=-Math.pow(2,63) && x<=Math.pow(2,63)-1){
                    System.out.println("* long");
                }
                
            }
            catch(Exception e)
            {
                System.out.println(sc.next()+" can't be fitted anywhere.");
            }

        }
    }
}




```
