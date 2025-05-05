![image](https://github.com/user-attachments/assets/60972f81-52d6-42c1-9aaf-d3c6d9785676)

```cpp
import java.util.Scanner;
import java.util.TreeMap;
import java.util.TreeSet;
import java.util.ArrayList;
import java.util.HashMap;
import java.util.HashSet;
import java.util.LinkedHashSet;
import java.util.Map;
public class baiTapSetMap {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        TreeMap<Integer, Integer> map = new TreeMap<>();
        for(int i = 1; i <= n; i++){
            for(int j = 1; j <= n; j++){
                int x = sc.nextInt();
                if(i == 1){
                    map.put(x, 1);
                    }
                else{
                    if(map.containsKey(x) && map.get(x) == i - 1){
                        map.put(x, map.get(x) + 1);
                    }
                }
            }
        }
        boolean found = false;
        for(Map.Entry<Integer, Integer> entry : map.entrySet()){
            if(entry.getValue() == n ){
                found = true;
                System.out.println(entry.getKey());
            }
        }
        if(found == false){
            System.out.println("NOT FOUND");
        }
    }
}
```
