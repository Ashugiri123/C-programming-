import java.util.*;
public class Main{
    public static void Hanoi(int n,char source,char helper,char destination){
        if(n==1){
            System.out.println("shift"+ n+"disk from" + source+ " to " + destination);
            return;
        }
        Hanoi(n-1, source, destination, helper);
        System.out.println("shift"+n+"disk from" + source+ " to " + destination);
        Hanoi(n-1, helper, source, destination);
         return;}
    public static void main(String args[]){
        System.out.println("enter number of disk:");
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        Hanoi(n,'S','H','D');
    }
}
