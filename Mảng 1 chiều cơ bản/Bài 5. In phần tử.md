![Screenshot 2025-04-10 134414](https://github.com/user-attachments/assets/dda69e5c-7a45-477f-8977-2f310a6e77b4)

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
            boolean check = false;
            for(int i = 0; i < n; i+= 2){
                if(a[i]  %  2 == 0){
                    System.out.print(a[i] + " ");
                    check = true;
                }
            }
            if(!check){
                System.out.println("NONE");
            }
    }
    
}

```
