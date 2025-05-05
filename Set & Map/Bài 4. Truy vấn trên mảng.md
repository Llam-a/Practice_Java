![image](https://github.com/user-attachments/assets/a83fad0c-e256-4f06-9ef4-944d1017ab37)

```java
package hoclaptrinhjava;
import java.util.*;

    public class Buoi1 {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            int n = sc.nextInt();
            HashMap<Integer, Integer> mp = new HashMap<>();
            for(int i = 0; i < n; i++){
                int x = sc.nextInt();
                if(mp.containsKey(x)){
                    mp.put(x, mp.get(x) + 1);
                }else{
                    mp.put(x,1);
                }
            }
            int q = sc.nextInt();
            while(q-- > 0){
                int tt = sc.nextInt();
                if(tt == 1){
                    int x = sc.nextInt();
                    if(mp.containsKey(x)){
                        mp.put(x, mp.put(x, mp.get(x) + 1));
                    }else{
                        mp.put(x,1);
                    }
                }else if(tt == 2){
                    int x = sc.nextInt();
                    if(mp.containsKey(x)){
                        mp.put(x,mp.get(x) - 1);
                            if(mp.get(x) == 0){
                                mp.remove(x);
                            }
                        }
                    }else{
                        int x = sc.nextInt();
                        if(mp.containsKey(x)){
                            System.out.println("YES");
                        }else{
                            System.out.println("NO");
                        }
                    }
                }
            }
    }
```
