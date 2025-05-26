![image](https://github.com/user-attachments/assets/4728ae84-081d-4232-86dd-b76e7703832b)

![image](https://github.com/user-attachments/assets/895ab645-e6d3-4dc1-8287-b5ef8e26f20e)

```java
import java.util.HashSet;
import java.util.Scanner;
import java.util.Set;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        Set<Integer> se = new HashSet<>();

        for (int i = 0; i < n; i++) se.add(sc.nextInt());
        sc.close();

        System.out.println(se.size());

        System.exit(0);
    }
}

```
