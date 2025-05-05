![image](https://github.com/user-attachments/assets/e48bcd52-4e33-4182-9636-d4724a92e6fc)

```
package hoclaptrinhjava;
import java.util.*;

    public class Buoi1 {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            int n = sc.nextInt();
            LinkedHashSet<Integer> set = new LinkedHashSet<>();
            for(int i = 0; i < n; i++){
                set.add(sc.nextInt());
            }
            for(int x : set){
                System.out.print(x + " ");
            }
            sc.close();
    }
}
```
