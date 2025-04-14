![Screenshot 2025-04-10 135137](https://github.com/user-attachments/assets/cd60e130-0ecc-4f33-86aa-7f793946b179)

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
            int[] count = new int[1001];
            for(var x : a){
                count[x]++;
            }
            for(int i = 0; i < n; i++){
                if(count[a[i]] > 0){
                    System.out.println(a[i] + " " + count[a[i]]);
                    count[a[i]] = 0;
                }

            }

    }
    
}

```
