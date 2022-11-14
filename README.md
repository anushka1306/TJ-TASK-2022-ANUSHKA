# TJ-TASK-2022-ANUSHKA
**Question 1:**
class Solution {
    public boolean isPowerOfTwo(int n) {
        // Base cases as '1' is the only odd number which is a power of 2 i.e. 2^0...
        if(n==1)
            return true;
        // All other odd numbers are not powers of 2...
        else if (n % 2 != 0 || n == 0)
            return false;
        // Recursive function call
        return isPowerOfTwo(n/2);
    }
}
![image](https://user-images.githubusercontent.com/118106624/201599415-5e0d28e0-4877-469e-a4c6-6b9cdf32425c.png)
**end of question 1**
**Question 2:**
class Solution {
    public int commonFactors(int a, int b) {
        int n = gcd(a, b);
 
        // Count divisors of n.
        int result = 0;
        for (int i = 1; i <= n; i++) {
            // if 'i' is factor of n
            if (n % i == 0) {
                result++;
            }
        }
        return result;
    }
    static int gcd(int a, int b){
        if (a == 0)
            return b;
 
        return gcd(b % a, a);
    }
}
class Solution {
    public int commonFactors(int a, int b) {
        int n = gcd(a, b);
 
        // Count divisors of n.
        int result = 0;
        for (int i = 1; i <= n; i++) {
            // if 'i' is factor of n
            if (n % i == 0) {
                result++;
            }
        }
        return result;
    }
    static int gcd(int a, int b){
        if (a == 0)
            return b;
 
        return gcd(b % a, a);
    }
}
class Solution {
    public int commonFactors(int a, int b) {
        int n = gcd(a, b);
 
        // Count divisors of n.
        int result = 0;
        for (int i = 1; i <= n; i++) {
            // if 'i' is factor of n
            if (n % i == 0) {
                result++;
            }
        }
        return result;
    }
    static int gcd(int a, int b){
        if (a == 0)
            return b;
 
        return gcd(b % a, a);
    }
}
![image](https://user-images.githubusercontent.com/118106624/201597882-04a26fa5-5883-477f-872f-1fae064566f9.png)

**end of question 2**
**Question 3:**
class Solution {
    public int maximum69Number (int num) {
        String str = String.valueOf(num);
        char[] arr = str.toCharArray();
        for(int i = 0; i< str.length(); i++){
            if(arr[i] == '6') {
                arr[i] = '9';
                break;
            }
        }
        return Integer.parseInt(String.valueOf(arr));
    }
}
![image](https://user-images.githubusercontent.com/118106624/201601166-b7ece586-b815-4dfd-bcae-0fec4c6478f4.png)
class Solution {
    public int maximum69Number (int num) {
        String str = String.valueOf(num);
        char[] arr = str.toCharArray();
        for(int i = 0; i< str.length(); i++){
            if(arr[i] == '6') {
                arr[i] = '9';
                break;
            }
        }
        return Integer.parseInt(String.valueOf(arr));
    }
}
**end of question 3**
