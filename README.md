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
