# TJ-TASK-2022-ANUSHKA
**DSA-CP easy tasks:**
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
    public int findMaxK(int[] nums) {
        Set<Integer> set = new HashSet<>();
        for (int i = 0; i < nums.length; i++){
            set.add(nums[i]);
			}
        int ans = -1;
        for (int i = 0; i < nums.length; i++) {
            if (nums[i] > ans && set.contains(-nums[i]))
                ans = nums[i];
        }
        return ans;
    }
}
![image](https://user-images.githubusercontent.com/118106624/201619880-d7131528-07cd-40f8-925c-cc306bc694d2.png)
** end of quetion 2 **
**Question 3:**
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

**end of question 3**
**Question 4:**
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
**end of question 4**
**end of DSA easy tasks**
**DSA medium tasks:**
**Quetion 1:**
class Solution {
    public int longestSubarray(int[] nums) {
        int max = 0;
        for (int i : nums) {
            if (i > max) max = i;
        }
        
        int maxLen = 0, currLen = 0;
        
        for (int n : nums) {
            if (n == max) currLen++;
            else currLen = 0;
            maxLen = Math.max(maxLen, currLen);
        }
        
        return maxLen;
    }
}
![image](https://user-images.githubusercontent.com/118106624/201625145-a8de33f5-f552-43d0-8c50-99ae876b3d6e.png)
**end of question 1**	
**Question 2:**
class Solution {
    public int minGroups(int[][] intervals) {
        int[] count = new int[1000002];
        
        for(int[] in : intervals){
            count[in[0]]++;
            count[in[1]+1]--;
        }
        
        int max = 0;
            
        for(int i = 1; i < 1000002; i++){
            count[i] += count[i-1];
            max = Math.max(max, count[i]);
        }
        
        return max;
    }
}
![image](https://user-images.githubusercontent.com/118106624/201626703-d76b556a-43e2-499b-ba98-72ab74555ad7.png)	
**end of question 2**	
**Question 3:**
class Pair{
    String name="";
    String id="";
    long view=0L;
    long maxi=0;
    Pair(String name,String id,int vi){
        this.name=name;
        this.id=id;
        view=vi;
        maxi=Math.max(maxi,vi); // to get to know whether the pariticular creator's id has the maximum view so as to get lexicographically smallest id.
    }
}
class Solution {
    public List<List<String>> mostPopularCreator(String[] creators, String[] ids, int[] views) {
        Map<String,Pair> map=new TreeMap<>();
        long max=0L;
   
        for(int i=0;i<creators.length;i++){
            if(!map.containsKey(creators[i])){
             Pair temp=new Pair(creators[i],ids[i],views[i]);
                map.put(creators[i],temp);
            }
            else{
                Pair temp=map.get(creators[i]);
               
                if(temp.maxi<views[i] || (temp.maxi==views[i] && ids[i].compareTo(temp.id)<0)){
                    temp.id=ids[i];
                    temp.maxi=views[i];
                }
                 temp.view=temp.view+views[i];
            }
            max=Math.max(max,map.get(creators[i]).view);
        }
       
        List<List<String>>res=new ArrayList<>();
        for(Map.Entry<String,Pair> en:map.entrySet()){
           if(en.getValue().view==max){
               List<String> ls=new ArrayList<>();
               ls.add(en.getKey());
               ls.add(en.getValue().id);
               res.add(new ArrayList<>(ls));
           }
        }

        return res;
        
        
    }
}
![image](https://user-images.githubusercontent.com/118106624/201634038-d31da4cd-d12d-40b5-8089-9d483e364562.png)
		
**end of question 3**
**end of DSA medium tasks**			   
