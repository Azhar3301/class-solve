problem 1:
import java.util.*;
public class Solution {
public static void main(String[] args) {
    Scanner sc=new Scanner(System.in);
    int x=sc.nextInt();
        int sum=0,t=x;
        while(t>0){
            sum+=t%10;
            t/=10;
        }
        if(x%sum==0)System.out.println("Harshad number");
        else System.out.println("not a Harshad number");
    }
    
}



problem 2 solution:
class Solution {
public int sumOfTheDigitsOfHarshadNumber(int x) {
        int sum=0,t=x;
        while(t>0){
            sum+=t%10;
            t/=10;
        }
        return(x%sum==0)?sum:-1;
    }
};


problem 3:
import java.util.*;
public class Main {
    public static void main(String[] args) {
int n = 1000000;
        boolean[] g = new boolean[n + 1];
        for (int i = 1; i <= n; i++) {
            int s = i, t = i;
            while (t > 0) {
                s += t % 10;
                t /= 10;
            }
            if (s <= n) g[s] = true;
        }boolean[] p = new boolean[n + 1];
        Arrays.fill(p, true);
        p[0] = p[1] = false;
  for (int i = 2; i * i <= n; i++) {
            if (p[i]) {
                for (int j = i * i; j <= n; j += i) p[j] = false;
            }
        }
  int[] pre = new int[n + 1];
        for (int i = 1; i <= n; i++) {
            pre[i] = pre[i - 1] + ((!g[i] && p[i]) ? 1 : 0);
        }
        Scanner sc = new Scanner(System.in);
        int q = sc.nextInt();
        while (q-- > 0) {
            int a = sc.nextInt();
            int b = sc.nextInt();
            System.out.println(pre[b] - pre[a == 0 ? 0 : a - 1]);
        }
    }
}
