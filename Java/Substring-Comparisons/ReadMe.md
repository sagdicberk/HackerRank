# Problem 

## Code
```java
        for (int i = 0; i < s.length() - k; i++) {
            String temp = s.substring(i, i + k);
            
            if (temp.compareTo(smallest) < 0) {
                smallest = temp;
            }
            
            if (temp.compareTo(largest) > 0) {
                largest = temp;
            }
        }
```
