![image](https://github.com/user-attachments/assets/3d3cce5f-8292-4ad6-b4af-18ae7a2082ad)

```java
import java.util.Scanner;
import java.util.TreeMap;
import java.util.TreeSet;
import java.util.ArrayList;
import java.util.HashMap;
import java.util.HashSet;
import java.util.LinkedHashSet;
import java.util.Map;

    public class Buoi1 {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            int n = sc.nextInt();
            TreeSet<Integer> set = new TreeSet<>();
            for(int i = 0; i < n; i++){
                set.add(sc.nextInt());
            }
            int q = sc.nextInt();
            while(q-- > 0){
                int tt = sc.nextInt();
                if(tt == 1){
                    set.add(sc.nextInt());
                }else if(tt == 2){
                    int x = sc.nextInt();
                    if(set.contains(x)){
                        set.remove(x);
                    }
                }else if(tt == 3){
                    System.out.println(set.first());
                }else{
                    System.out.println(set.last());
                }
            }
        sc.close();
    }
}
```
