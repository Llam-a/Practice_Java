![image](https://github.com/user-attachments/assets/b7ca5c44-1b1e-4f93-9d70-459fbc934d85)

![image](https://github.com/user-attachments/assets/9881c15e-5a0e-4389-8263-ca57cd321032)

```java
import java.util.Scanner;
import java.util.Collections;
import java.util.Comparator;
import java.util.ArrayList;

public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt(), x = sc.nextInt();
        ArrayList<Integer> arr = new ArrayList<>();

        for (int i = 0; i < n; ++i) arr.add(sc.nextInt());
        sc.close();

        Collections.sort(arr, new Comparator<Integer>(){
            @Override
            public int compare(Integer o1, Integer o2) {
                int s1 = Math.abs(o1 - x), s2 = Math.abs(o2 - x);
                return (s1 != s2) ? s1 - s2 : o1 - o2;
            }
        });

        for (var i : arr) System.out.print(i + " ");
        System.out.println();

        Collections.sort(arr, new Comparator<Integer>() {
            @Override
            public int compare(Integer o1, Integer o2)
            {
                int s1 = o1 % 2, s2 = o2 % 2;

                if (s1 == 1 && s2 == 1) return o2 - o1;
                else if (s1 == 0 && s2 == 0) return o1 - o2;
                return s1 - s2;
            }
        });

        for (var i : arr) System.out.print(i + " ");

        System.exit(0);
    }
}
```
