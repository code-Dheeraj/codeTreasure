# codeTreasure
// ***************************************************************************************************************************************************************************
// code for storing long integer values in JAVA by using BigInteger 
// que:- You are asked to calculate factorials of some small positive integers.(An integer t, 1<=t<=100, denoting the number of testcases, followed by t lines, each containing a //single integer n, 1<=n<=100.)

import java.math.BigInteger;
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) 
	{
	    Scanner input=new Scanner(System.in);
		int t=input.nextInt();
		
	    for(int k=0;k<t;k++)
	    {
		    BigInteger fact=BigInteger.valueOf(1);
		    int num=input.nextInt();
		    for(int i=num; i>0; i--)
		    {
		        fact = fact.multiply(BigInteger.valueOf(i));
		    }
		    System.out.println(fact);
		}
		
	}
}
// note : if we want to store large value in java than we can we BigInteger and if we you want to know more about BigIntefer than
// you might check on this 
//https://www.geeksforgeeks.org/biginteger-class-in-java/#:~:text=BigInteger%20class%20is%20used%20for,all%20available%20primitive%20data%20types.

// ***************************************************************************************************************************************************************************




import java.util.Arrays;
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) 
	{
	   Scanner input=new Scanner(System.in);
	   int t=input.nextInt();
	   int[][] x=new int[2][5];
	   for(int i=0;i<t;i++)
	   {
	       x[0][i]=input.nextInt();
	       x[1][i]=input.nextInt();
	   }
	   int[] res1=new int[t];
	   int[] res2=new int[t];
	   for(int j=0;j<t;j++)
	   {
	       res1[j]=( x[0][j]-x[1][j]);
	       res2[j]=( x[1][j]-x[0][j]);
	   }
	   Arrays.sort(res1);
	   Arrays.sort(res2);
	   if(res1[t-1]>res2[t-1]){
	       System.out.println("1 "+ res1[t-1]);
	   }
	   else{
	       System.out.println("2 "+ res2[t-1]);
	   }
	
	}
}

