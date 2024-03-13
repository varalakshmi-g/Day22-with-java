# Day22-with-java

Hello everyone today I learned and practicedhow to print common elements in an array.

here is the program for that.

import java.util.Scanner;
public class Day22{
    public static void main(String[] args)
{
    Scanner scan = new Scanner(System.in);
    int n = scan.nextInt();
    int[] ar1 = new int[n];
    for(int i = 0; i < ar1.length; i++) {
        ar1[i] = scan.nextInt();
        
    }
    int m = scan.nextInt();
    int[] ar2 = new int[n];
    for(int j = 0; j < ar2.length; j++) {
        ar2[j] = scan.nextInt();
        
    }
    printCommonElements(ar1, ar2);
    
}
public static void printCommonElements(int[] ar1, int[] ar2)
{
    int i=0, j=0;
    while(i<ar1.length && j<ar2.length)
    {
        if (ar1[i] == ar2[j])
        {
            System.out.println(ar1[i]);
            i++;
            j++;
        }
        else if(ar1[i] > ar2[j])
        {
            j++;
        }
        else
        {
            i++;
        }
    }
}
}

output:
Size of the array1 : 5
Elements of the array1: 2 3 4 5 6
Size of the array2 : 5
Elements of the array2: 1 2 5 6 8
Common elements are: 2 5 6



