![Screenshot 2025-04-10 095006](https://github.com/user-attachments/assets/3412595e-aaa9-4b03-bdb1-1484b220382e)

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
            int count = 0, sum = 0;
            for(var x : a){
                if(isPrimes(x)){
                    ++count;
                    sum += x;
                }
            }
            double avg = 0.1 * sum / count;
            System.out.printf("%3f", avg);
            sc.close();
    }
    
}

```
