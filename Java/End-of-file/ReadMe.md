# Problem
The challenge here is to read  lines of input until you reach EOF, then number and print all  lines of content.

Hint: Java's Scanner.hasNext() method is helpful for this problem.
Refence: https://en.wikipedia.org/wiki/End-of-file

## Quick Explanation
First, it's important to understand the concept of EOF (End-of-File). EOF signifies that there is no more input for the program to read, allowing the program to exit gracefully.

To indicate EOF manually, you can use keyboard shortcuts:

Intelij IDE Bash: 'CTRL + D'

In this solution, I use StringBuilder to efficiently build and format the output as strings.

## Code
```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        
           Scanner sc = new Scanner(System.in);
        StringBuilder All = new StringBuilder();
        int lineNumber = 1;

        while(sc.hasNext()){

            All.append(lineNumber).append(" ").append(sc.nextLine()).append("\n");
            lineNumber++;
        }
        sc.close();
        All.setLength(All.length() - 1);

        System.out.println(All);
        
    }
}
```
