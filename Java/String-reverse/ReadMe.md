# Problem
A palindrome is a word, phrase, number, or other sequence of characters which reads the same backward or forward.

Given a string , print Yes if it is a palindrome, print No otherwise.
## Code
```java
  StringBuilder B = new StringBuilder(A);
  B.reverse();
  if (A.equals(B.toString())) {
  System.out.println("YES");
  }
```
