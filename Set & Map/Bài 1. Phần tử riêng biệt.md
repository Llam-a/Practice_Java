![Screenshot 2025-05-05 084339](https://github.com/user-attachments/assets/d14b5a25-2702-4b11-8164-a99fa1c2136c)

```java
package hoclaptrinhjava;
import java.util.*;

    public class Buoi1 {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            int n = sc.nextInt();
            HashSet<Integer> set = new HashSet<>();
            for(int i = 0; i < n; i++){
                set.add(sc.nextInt());
            }
            System.out.println(set.size());
            sc.close();
    }
}
```
