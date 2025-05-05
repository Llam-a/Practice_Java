![image](https://github.com/user-attachments/assets/a7c49a18-0f87-4781-afe3-f1e3975b64b9)

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
            TreeMap<Character, Integer> b = new TreeMap<>();
            for(int i = 0; i < n; i++){
                Character c = sc.next().charAt(0);
                if(b.containsKey(c)){
                    int f = b.get(c);
                    b.put(c, f + 1);
                }else{
                    b.put(c, 1);
                }
            }
            System.out.println(b.firstKey() + " " + b.get(b.firstKey()));
            System.out.println();
            System.out.println(b.lastKey() + " " + b.get(b.lastKey()));
            System.out.println();
            for (Map.Entry<Character, Integer> entry : b.entrySet()) {
                Character key = entry.getKey();
                Integer value = entry.getValue();
                System.out.println(key+" "+value);
            }
            System.out.println();
            TreeMap<Character, Integer> reversedMap = new TreeMap<>(b.descendingMap());
            for (Map.Entry<Character, Integer> entry : reversedMap.entrySet()) {
                Character key = entry.getKey();
                Integer value = entry.getValue();
                       System.out.println(key+" "+value);
        }
        sc.close();
    }
}
```
