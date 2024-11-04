```java
static boolean isAnagram(String a, String b) {
        int n = a.length();
        int m = b.length();

        a = a.toLowerCase();
        b = b.toLowerCase();

        if (n != m)
            return false;

        int freq[] = new int[255];
        for (int i = 0; i < n; i++) {
            freq[a.charAt(i)]++;
            freq[b.charAt(i)]++;
        }

        System.out.println("Character frequencies:");
        for (int i = 0; i < 255; i++) {
            if (freq[i] > 0) {  // Sadece frekansı sıfırdan büyük olan karakterleri yazdır
                System.out.println((char)i + ": " + freq[i]);
            }
        }

        for (int i = 0; i < n; i++) {
            if (freq[a.charAt(i)] % 2 != 0)
                return false;
        }

        return true;

    }
```
