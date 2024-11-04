```java
static boolean isAnagram(String a, String b) {
        
        if (a.length() != b.length()) {
            return false;
        }
        
        char[] charArray1 = a.toLowerCase().toCharArray();
        char[] charArray2 = b.toLowerCase().toCharArray();
        
        Arrays.sort(charArray1);
        Arrays.sort(charArray2);
        
        return Arrays.equals(charArray1, charArray2);

    }
```
