![Screenshot 2025-04-10 134509](https://github.com/user-attachments/assets/36750ad0-bad6-44c2-850e-8dae77e70730)

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
            int cnt = 0;
            for(int i = 0; i < n; i++){
                for(int j = i + 1; j < i; j++){
                    if(a[i] == a[j]){
                        cnt++;
                    }
                }
            }
            System.out.println(cnt);
    }
    
}
```
