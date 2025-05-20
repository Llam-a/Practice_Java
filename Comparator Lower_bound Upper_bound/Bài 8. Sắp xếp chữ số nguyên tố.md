![image](https://github.com/user-attachments/assets/edec3a5b-16e7-465a-b0f6-e5561ad53daf)

![image](https://github.com/user-attachments/assets/3786494e-e5f6-4c37-8067-807920edd05d)

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
        ArrayList<Integer> a = new ArrayList<>();
        for(int i = 0; i < n; i++){
            a.add(sc.nextInt());
        }
        Collections.sort(a, new Comparator<Integer>(){
            public int compare(Integer a, Integer b){
                if(cntPrime(a) != cntPrime(b)){
                    return cntPrime(b) - cntPrime(a);
                }else{
                    return 0;
                }
            }
        });
        for(int x : a){
            System.out.print(x + " ");
        }
    }
}
```
