# Problem
Given a square matrix, calculate the absolute difference between the sums of its diagonals.

For example, the square matrix  is shown below:

1 2 3
4 5 6
9 8 9  
The left-to-right diagonal = . The right to left diagonal = . Their absolute difference is .

Function description

Complete the  function in the editor below.

diagonalDifference takes the following parameter:

int arr[n][m]: an array of integers
## Code 
```java
  public static int diagonalDifference(List<List<Integer>> arr) {
        // Write your code here
        int firstDiagonalSum = 0;
        int secondDiagonalSum = 0;
        int arrSize = arr.size();

        for (int i = 0; i < arrSize; i++) {

            firstDiagonalSum += arr.get(i).get(i);
            secondDiagonalSum += arr.get(i).get(arrSize - 1 - i);
        }

        return Math.abs(firstDiagonalSum - secondDiagonalSum);
    }
```
