# Problem
Given a string, , matching the regular expression [A-Za-z !,?._'@]+, split the string into tokens. We define a token to be one or more consecutive English alphabetic letters. Then, print the number of tokens, followed by each token on a new line.

Note: You may find the String.split method helpful in completing this challenge.

Input Format

A single string, .

Constraints

 is composed of any of the following: English alphabetic letters, blank spaces, exclamation points (!), commas (,), question marks (?), periods (.), underscores (_), apostrophes ('), and at symbols (@).

## Code
```java
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        String s = scan.nextLine();
        // Write your code here.
        scan.close();
        String[] sArray = s.split("[ !,?._'@]+");

        List<String> filteredList = new ArrayList<>();
        for (String str : sArray) {
            if (!str.isBlank()){
                filteredList.add(str);
            }
        }

        System.out.println(filteredList.size());
        filteredList.stream().forEach(System.out::println);
    }
}
```
