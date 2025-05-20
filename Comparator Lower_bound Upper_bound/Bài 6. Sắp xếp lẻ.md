![image](https://github.com/user-attachments/assets/36ff757e-df8c-4ae8-87dc-6552dc02aed9)

![image](https://github.com/user-attachments/assets/6e8a3771-752a-4a04-8dbf-066e67e6a8b3)

```java
import java.util.*;

public class Bai1 {
    public static int cntOdd(int n){
        int res =0;

        while(n != 0) {
            if((n % 10) % 2 != 0) res++;
            n /= 10;
        }

        return res;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();
        ArrayList<Integer> arr = new ArrayList<Integer>();
        for(int i = 0; i < n; i++){
            arr.add(sc.nextInt());
        }
        Collections.sort(arr, new Comparator<Integer>(){
            public int compare (Integer a, Integer b){
                if(cntOdd(a) != cntOdd(b)){
                    return cntOdd(b) - cntOdd(a);
                }else{
                    return a - b;
                }
            }
        });
        for(int x : arr){
            System.out.print(x + " ");
        }
    }
}
```
