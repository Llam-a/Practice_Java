![Screenshot 2025-04-10 134356](https://github.com/user-attachments/assets/63310955-b254-420a-8eb0-4cc7eeec147d)

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
            int t = sc.nextInt();
            int count_greater = 0;
            int count_less = 0;
            for(var x : a){
                if(x > t){
                    count_greater++;
                }else if(x < t){
                    count_less++;

                }
            }
            System.out.println(count_less + " " + count_greater);

    }
    
}

```
