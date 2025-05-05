![Screenshot 2025-05-05 091047](https://github.com/user-attachments/assets/099d3e5c-f69a-47f0-8866-453199eb1c21)

```java
package hoclaptrinhjava;
import java.util.*;

    public class Buoi1 {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            int n = sc.nextInt();
            HashSet<Integer> set = new HashSet<>();
            for(int i = 0; i < n; i++){
                set.add(sc.nextInt());
            }
            int q = sc.nextInt();
            while(q-- > 0){
                int x = sc.nextInt();
                if(set.contains(x)){
                    System.out.println("YES");
                }else{
                    System.out.println("NO");
                }
            }
            sc.close();
    }
}
```
