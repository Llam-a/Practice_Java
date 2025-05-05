![image](https://github.com/user-attachments/assets/3062ec95-15d7-422d-861a-7e10b40ecb35)

```java
import java.util.Scanner;
import java.util.TreeMap;
import java.util.TreeSet;
import java.util.ArrayList;
import java.util.Collections;
import java.util.HashMap;
import java.util.HashSet;
import java.util.LinkedHashSet;
import java.util.Map;

    public class Buoi1 {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            TreeSet<Integer> set = new TreeSet<>(Collections.reverseOrder());
            int n = sc.nextInt(), m = sc.nextInt();
            for(int i = 0; i < n; i++){
                set.add(sc.nextInt());
            }
            for(int i = 0; i < m; i++){
                set.add(sc.nextInt());
            }
            for(int x : set){
                System.out.print(x + " ");
            }
        sc.close();
    }
}
```
