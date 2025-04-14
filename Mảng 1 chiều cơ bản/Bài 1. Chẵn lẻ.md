![Screenshot 2025-04-10 093738](https://github.com/user-attachments/assets/3ae6179c-3725-4596-8093-44c9d6754ac1)

```java
package hoclaptrinhjava;
import java.util.Scanner;

public class Buoi1 {

    public static final int MOD = 1000000007;
    public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            int n  = sc.nextInt();
            int[] a = new int[n];
            for(int i = 0; i < n; i++){
                a[i] = sc.nextInt();
            }
            int count_even = 0, count_odd = 0;
            int sum_even = 0, sum_odd = 0;
            for(var x : a){
                if(x % 2 == 0){
                    count_even++;
                    sum_even += x;
                }else{
                    count_odd++;
                    sum_odd += x;
                }
            }
            System.out.println(count_even);
            System.out.println(sum_even);
            System.out.println(count_odd);
            System.out.println(sum_odd);



    }
}
```
