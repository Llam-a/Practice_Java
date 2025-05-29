![image](https://github.com/user-attachments/assets/9d4091d6-d712-4636-a492-2e38733afa70)

![image](https://github.com/user-attachments/assets/74ec6a63-7e74-4370-8b68-007d0cf2902e)

```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        ArrayList<Long> arr = new ArrayList();

        for(int i = 0; i < n; i++) arr.add(sc.nextLong());

        Collections.sort(arr);

        int q = sc.nextInt();
        while(q-- != 0) {
            long k = sc.nextLong();
            if(Collections.binarySearch(arr, k) >= 0) System.out.println("YES");
            else System.out.println("NO");
        }

        sc.close();
        
        System.exit(0);
    }
}
```
