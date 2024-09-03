# JAVA
CONTROL FLOWSTATEMENTS 1 ASSIGNMENT
1]Java program to generate electricity bill .
import java.util.*;
public class B
{
public static void main(String[] args) {
   Scanner sc=new Scanner(System.in);
   double Amt=1,pr,cr,a;
   System.out.println("enter current reading:");
   cr=sc.nextDouble();
   System.out.println("enter previous reading:");
   pr=sc.nextDouble();
   if(cr<pr || cr<0 || pr<0)
   {
       System.out.println("Invalid reading");
       Amt=0;
   }
   else
   {
      a=cr-pr;
      if(a>0 && a<=50)
      {
          Amt=a*1.50;
      }
      else if(a>=51 && a<=100)
      {
          a=a-50;
          Amt=50*1.50+a*2.00;
      }
      else if(a>=101 && a<=150)
            {  a=a-100;
Amt=50*1.50+50*2.00+a*3.50;     }
      else if(a>=151)
      {
          a=a-150;
          Amt=50*1.50+50*2.00+50*3.50+a*5.00;
      }
   }
   if(Amt<100 && Amt!=0)
   {
       Amt=100;
       System.out.println("bill is:"+Amt);
   }
   else
   {
       System.out.println("bill amount is:"+Amt);
   }
}
}

