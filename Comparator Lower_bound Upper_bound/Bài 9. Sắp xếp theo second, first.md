![image](https://github.com/user-attachments/assets/cc48382b-8c9a-4f76-93e7-5d16890fd6a8)

```
INPUT01
15
63 40
19 28
4 48
26 64
52 46
76 86
16 81
57 28
54 95
80 10
17 36
10 19
37 74
9 55
32 85
OUTPUT01
80 10
10 19
57 28
19 28
17 36
63 40
52 46
4 48
9 55
26 64
37 74
16 81
32 85
76 86
54 95
```

```java
import java.util.*;

public class Bai1 {
    public static int cntPrime(int n){
        int res = 0;
        while(n > 0){
            if(n % 10 == 2 || n % 10 == 3 || n % 10 == 5 || n % 10 == 7){
                ++res;
            }
            n/=10;
        }
        return res;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        ArrayList<ArrayList<Integer>> arr = new ArrayList<>();
        for(int i = 0; i < n; i++){
            ArrayList<Integer> list = new ArrayList<>();
            list.add(sc.nextInt());
            list.add(sc.nextInt());
            arr.add(list);
        }
        Collections.sort(arr, new Comparator<ArrayList<Integer>>(){
            public int compare(ArrayList<Integer> a, ArrayList<Integer> b){
                if(a.get(1) != b.get(1)) return a.get(1) - b.get(1);
                else return b.get(0) - a.get(0);
            }
        });
        for(var x : arr) System.out.println(x.get(0) + " " + x.get(1));
    }
}
```
