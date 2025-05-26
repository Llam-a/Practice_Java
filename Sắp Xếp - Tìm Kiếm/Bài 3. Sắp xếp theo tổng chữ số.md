![image](https://github.com/user-attachments/assets/1f276a86-1bdf-4a3f-bf8f-33692a719bac)

![image](https://github.com/user-attachments/assets/1c4b2444-104e-431a-8765-9791e6e8d7fb)

```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.Comparator;
import java.util.Scanner;

public class Main {
    public static int Sum_Of_Digits(int n) {
        int res = 0;

        while (n != 0) {
            res += n % 10;
            n /= 10;
        }

        return res;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        ArrayList<Integer> arr = new ArrayList<>();

        for (int i = 0; i < n; i++) arr.add(sc.nextInt());
        sc.close();

        Collections.sort(arr, new Comparator<Integer>() {
            @Override
            public int compare(Integer o1, Integer o2) {
                if (Sum_Of_Digits(o1) != Sum_Of_Digits(o2)) return Sum_Of_Digits(o1) - Sum_Of_Digits(o2);
                return o1 - o2;
            }
        });

        for (var i : arr) System.out.print(i + " ");

        System.exit(0);
    }
}
```
