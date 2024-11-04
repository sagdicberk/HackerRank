# Problem 

We define the following terms:

Lexicographical Order, also known as alphabetic or dictionary order, orders characters as follows:

For example, ball < cat, dog < dorm, Happy < happy, Zoo < ball.

A substring of a string is a contiguous block of characters in the string. For example, the substrings of abc are a, b, c, ab, bc, and abc.
Given a string, , and an integer, , complete the function so that it finds the lexicographically smallest and largest substrings of length .

Function Description

Complete the getSmallestAndLargest function in the editor below.

getSmallestAndLargest has the following parameters:

string s: a string
int k: the length of the substrings to find

## Code
```java
public static String getSmallestAndLargest(String s, int k) {
        String smallest = s.substring(0, k);
        String largest = s.substring(0, k);


        // Complete the function
        // 'smallest' must be the lexicographically smallest substring of length 'k'
        // 'largest' must be the lexicographically largest substring of length 'k'

        for (int i = 0; i < s.length() - k +1; i++) {
            String temp = s.substring(i, i + k);

            if (temp.compareTo(smallest) < 0) {
                smallest = temp;
            }

            if (temp.compareTo(largest) > 0) {
                largest = temp;
            }
        }

        return smallest + "\n" + largest;
    }
```
