![image](https://github.com/user-attachments/assets/951ef09b-e13c-46b5-89ad-23bc170cd4d4)

![image](https://github.com/user-attachments/assets/17d1a62b-6b34-4cc1-848d-d31aef1dfad0)

```java
import java.util.*;
import java.util.Comparator;
public class Main {

    public static boolean cmp1(int a, int b) {
        int countA = 0, countB = 0;
        int tempA = a, tempB = b;

        while (tempA > 0) {
            int digit = tempA % 10;
            if (digit == 0 || digit == 6 || digit == 8)
                countA++;
            tempA /= 10;
        }

        while (tempB > 0) {
            int digit = tempB % 10;
            if (digit == 0 || digit == 6 || digit == 8)
                countB++;
            tempB /= 10;
        }

        if (countA != countB) {
            return countA > countB;
        } else {
            return a < b;
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        Integer[] a = new Integer[n];


        for (int i = 0; i < n; i++) {
            a[i] = sc.nextInt();
        }

        Arrays.sort(a, new Comparator<Integer>() {
            public int compare(Integer x, Integer y) {
                if (cmp1(x, y))
                    return -1;
                else
                    return 1;
            }
        });

        for (int x : a) {
            System.out.print(x + " ");
        }

        sc.close();
    }
}
```
