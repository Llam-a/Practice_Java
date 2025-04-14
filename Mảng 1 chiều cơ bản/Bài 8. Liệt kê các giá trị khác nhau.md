![Screenshot 2025-04-10 134913](https://github.com/user-attachments/assets/abe1e7a8-8b2e-43d0-8967-2b2baa6158c9)

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
            for(int i = 0; i < n; i++){
                boolean flag = false;
                for(int j = 0; j <= i - 1; j++){
                    if(a[i] == a[j]){
                        flag = true;
                        break;
                    }
                }
                if(flag == false){
                    System.out.println(a[i] + " ");
                }
            }
    }
    
}
```
