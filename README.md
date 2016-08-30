# Leetcode questions
[![Motto](https://img.shields.io/badge/motto-good%20good%20study%2C%20day%20day%20up-red.svg)](https://en.wikipedia.org/wiki/Day_Day_Up)

We will working on the Leetcode questions! Unit tests are recommended.

### Questions table

|Question:Remove Duplicates from Sorted Array |Unit test:161 cases: |Runtime Beat:54.77%: |Author: Cory|

public class solutuion{

  public int removeDupulcates(int[] nums ){
     
      int start = 0;
      
      for(int i = 1; i < nums.length;i++){
          if(nums[i] != nums[start]){
            nums[++start] = nums[i];
          }
      }
      return start + 1;
    }
  
}

|Question: Contains with most water| unit test:45  | Runtime beat: 78.10%   | Author: Cory  |

public class solution{

    public int containsWithMostWater(int[] height){
    
        if(height.length <= 1 || height == null) reurn 0;
        
        int max = 0, left = 0, right = height.length - 1, hLeft = height[left], hRight = height[right];
        
        while(left < right){
            max = Math.max(max, (right - left) * Math.min(hLeft, hRight));
            
            if(hLeft < hright){
                while(left < right && height[left] <= hLeft) left++;
                
                if(left < right) lLeft = height[left];
            }else{
                while(left < right && height[right] <= hRight) right--;
                
                if(left < right) hRight = height[right];
            }
          
          }
          
        return max;
    }
    
}
