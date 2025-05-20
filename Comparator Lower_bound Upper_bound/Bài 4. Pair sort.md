![image](https://github.com/user-attachments/assets/857f2f84-c4f6-4863-9b9a-b1314433126f)

```
INPUT01
13
-42 -76
47 43
12 7
-62 31
7 64
42 -92
-89 60
45 41
3 54
-41 40
20 -24
88 42
0 12

OUTPUT01
0 12
12 7
20 -24
3 54
-41 40
45 41
47 43
7 64
-62 31
-42 -76
88 42
42 -92
-89 60
```

```java
import java.util.ArrayList;
import java.util.Arrays;
import java.util.Collections;
import java.util.Comparator;
import java.util.HashMap;
import java.util.HashSet;
import java.util.LinkedHashMap;
import java.util.LinkedHashSet;
import java.util.Map;
import java.util.Scanner;
import java.util.TreeMap;
import java.util.TreeSet;

public class HocLapTrinhJava {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        ArrayList<Integer>[] a = new ArrayList[n];
        for(int i = 0; i < n; i++){
            a[i] = new ArrayList<>();
            a[i].add(sc.nextInt());
            a[i].add(sc.nextInt());
        }
        Arrays.sort(a, new Comparator<ArrayList<Integer>>(){
            public int compare(ArrayList<Integer> o1, ArrayList<Integer> o2){
                int d1 = o1.get(0) * o1.get(0) + o1.get(1) * o1.get(1);
                int d2 = o2.get(0) * o2.get(0) + o2.get(1) * o2.get(1);
                if(d1 != d2)
                    return d1 - d2;
                if(o1.get(0) != o2.get(0))
                    return o1.get(0) - o2.get(0);
                return o1.get(1) - o2.get(1);
            }
        });
        for(ArrayList<Integer> point : a){
            System.out.println(point.get(0) + " " + point.get(1));
        }
    }
}
```
