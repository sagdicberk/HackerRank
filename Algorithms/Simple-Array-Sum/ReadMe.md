# Problem 
Given an array of integers, find the sum of its elements.

For example, if the array , , so return .

Function Description

Complete the simpleArraySum function in the editor below. It must return the sum of the array elements as an integer.

simpleArraySum has the following parameter(s):

ar: an array of integers

## Code 
```java
public static int simpleArraySum(List<Integer> ar) {
  // Write your code here
  int sum = 0;
  for(int a : ar){
    sum += a;
  }
  return sum;
}
```
