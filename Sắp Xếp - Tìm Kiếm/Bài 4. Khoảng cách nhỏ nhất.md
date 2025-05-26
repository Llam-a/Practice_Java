![image](https://github.com/user-attachments/assets/dd3492d5-61c4-42ea-b959-baf59362b6b9)

![image](https://github.com/user-attachments/assets/39d4eab8-3551-4913-91d0-dbd56292e4c4)

```java
import java.util.*;
public class Bai1 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] a = new int[n];
        for(int i  = 0; i < n; i++){
            a[i] = sc.nextInt();
        }
        Arrays.sort(a);
        int res = Integer.MAX_VALUE;
        for(int i =  1; i < n; i++){
            res = Math.min(res, a[i] - a[i - 1]);
        }
        System.out.println(res);
    }
}
```
