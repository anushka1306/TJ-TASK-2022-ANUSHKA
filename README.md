# TJ-TASK-2022-ANUSHKA
import java.util.*;
//importing util package
class powerof2
{
    int x;
    //instance variable
    boolean isPowerOf2(int num)
    {
        //recursive function to check if the number is raised to the power of 2
        if(num==0)
        {
            return false;
        }
        if(num==1)
        {
            return true;
        }
        if(num%2!=0)
        {
            isPowerOf2(num/2);
            return false;
        }
        else
        {
           return true; 
        }
    }
    int calcx(int num)
    {
        //to calculate the value of x i.e. the power raised on base 2
        x=0;
        while(num!=0)
        {
            if(num%2==0)
            x++;
            num=num/2;
        }
        return x;
    }
    void main()
    {
        int n;
        Scanner sc=new Scanner(System.in);
        //declaration of scanner class
        powerof2 ob=new powerof2();
        //declaration of the object of the class
        System.out.println("Enter the number to be checked:");
        n=sc.nextInt();
        x=ob.calcx(n);
        if(ob.isPowerOf2(n)==true)
        {
            System.out.println("true\nExplanation: 2^"+x+"="+n);
        }
        else
        {
            System.out.println("false\nthe number entered is not a power of 2");
        }
    }
}
//end of program
![output 1](https://user-images.githubusercontent.com/118106624/201517864-acec180d-61c1-4d7e-8e3a-55572c4d2ae6.png)
![2022-11-13 (1)](https://user-images.githubusercontent.com/118106624/201517926-00252f95-c6b6-4b6e-ba07-42aaf8dae788.png)
![2022-11-13 (2)](https://user-images.githubusercontent.com/118106624/201517934-b9670c5e-04bf-4738-931c-6c70b675e218.png)
![2022-11-13 (3)](https://user-images.githubusercontent.com/118106624/201517944-6de6663e-22cc-4812-adbb-b872f17cefaa.png)

