![image](https://github.com/user-attachments/assets/b595225d-5083-4368-8106-20d7298955f3)

![image](https://github.com/user-attachments/assets/7f8142c5-c8c9-4e8c-8807-01164e7a368c)

```java
import java.util.Scanner;
import java.util.TreeMap;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        TreeMap<Integer, Integer> map = new TreeMap<>();

        for (int i = 0; i < n; i++) {
            int t = sc.nextInt();
            map.put(t, map.getOrDefault(t, 0) + 1);
        }
        sc.close();

        int tmp = 0, maxx = Integer.MIN_VALUE;

        for(var entry : map.entrySet()) {
            if(entry.getValue() > maxx) {
                maxx = entry.getValue();
                tmp = entry.getKey();
            }
        }

        System.out.println(tmp + " " + maxx);

        System.exit(0);
    }
}
```
