![image](https://github.com/user-attachments/assets/6db53098-13db-411e-a302-ea22370c5a54)

![image](https://github.com/user-attachments/assets/f1bf7a93-1a6a-4aa7-9a46-ff3553d62fcd)

```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.Comparator;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        ArrayList<Integer> arr = new ArrayList<>();

        for (int i = 0; i < n; i++) arr.add(sc.nextInt());
        sc.close();

        Collections.sort(arr, new Comparator<Integer>() {
            @Override
            public int compare(Integer o1, Integer o2) {
                return Math.abs(o1) - Math.abs(o2);
            }
        });

        for (var i : arr) System.out.print(i + " ");

        System.exit(0);
    }
}
```
