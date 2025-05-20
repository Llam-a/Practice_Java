![image](https://github.com/user-attachments/assets/d65399ae-7f8d-4da3-ac2f-9879f617d4d1)

![image](https://github.com/user-attachments/assets/4b535e7d-5130-435b-8900-de645573aaba)

```java
import java.util.*;

public class Bai1 {
    public static int countEven(int num) {
        int cnt = 0;
        while (num != 0) {
            int digit = num % 10;
            if (digit % 2 == 0) {
                cnt++;
            }
            num /= 10;
        }
        return cnt;
    }

    public static int countOdd(int num) {
        int cnt = 0;
        while (num != 0) {
            int digit = num % 10;
            if (digit % 2 != 0) {
                cnt++;
            }
            num /= 10;
        }
        return cnt;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        Integer[] a = new Integer[n];
        Integer[] b = new Integer[n];
        
        for (int i = 0; i < n; i++) {
            int x = sc.nextInt();
            a[i] = x;
            b[i] = x;
        }

        Arrays.sort(a, new Comparator<Integer>() {
            @Override
            public int compare(Integer a, Integer b) {
                int evenA = countEven(a);
                int evenB = countEven(b);
                if (evenA != evenB) {
                    return Integer.compare(evenA, evenB);
                } else {
                    return Integer.compare(a, b);
                }
            }
        });

        for (int x : a) {
            System.out.print(x + " ");
        }
        System.out.println();

        Arrays.sort(b, new Comparator<Integer>() {
            @Override
            public int compare(Integer a, Integer b) {
                int oddA = countOdd(a);
                int oddB = countOdd(b);
                if (oddA != oddB) {
                    return Integer.compare(oddA, oddB);
                } else {
                    return 0; 
                }
            }
        });

        for (int x : b) {
            System.out.print(x + " ");
        }
    }
}

```

