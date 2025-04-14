![Screenshot 2025-04-10 101406](https://github.com/user-attachments/assets/ab65ee91-3b48-4be1-98d5-60904489248d)

```java
package hoclaptrinhjava;
import java.util.Scanner;

public class Buoi1 {

    public static final int MOD = 1000000007;
    public static boolean isPrimes(long n){
        for(long i = 2; i <= Math.sqrt(n); i++){
            if(n % i == 0){
                return false;
            }
        }
        return n >= 2;
    }
    public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            int n  = sc.nextInt();
            int[] a = new int[n];
            for(int i = 0; i < n; i++){
                a[i] = sc.nextInt();
            }
            int min_value = Integer.MAX_VALUE;
            for(var x : a){
                if(x < min_value){
                    min_value = x;
                }
            }
            int cnt = 0;
            for(var x : a){
                if(x == min_value){
                    cnt++;
                }
            }
            System.out.print(cnt);

    }
    
}
```
