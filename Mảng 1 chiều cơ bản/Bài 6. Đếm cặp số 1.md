![Screenshot 2025-04-10 134509](https://github.com/user-attachments/assets/36750ad0-bad6-44c2-850e-8dae77e70730)

```java
package hoclaptrinhjava;
import java.util.Scanner;

public class Buoi1 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n  = sc.nextInt();
        int[] a = new int[n];
        for(int i = 0; i < n; i++){
            a[i] = sc.nextInt();
        }
        int k = sc.nextInt();
        int cnt = 0;
        for(int i = 0; i < n; i++){
            for(int j = i + 1; j < n; j++){
                if(a[i] + a[j] == k){
                    cnt++;
                }
            }
        }
        System.out.println(cnt);
        sc.close();
    }
}


```
