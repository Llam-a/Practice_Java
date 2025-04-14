![Screenshot 2025-04-10 134749](https://github.com/user-attachments/assets/ec9ff1bf-1938-48fd-9fef-83a6b28cf17a)

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
            for(int i = 0; i < n; i++){
                for(int j = i + 1; j < n; j++){
                    int dis = Math.abs(a[i] - a[j]);
                    min_value = Math.min(dis, min_value);
                }
            }
            System.out.println(min_value);
    }
    
}

```
