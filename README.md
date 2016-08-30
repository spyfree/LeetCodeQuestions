# Leetcode questions
[![Motto](https://img.shields.io/badge/motto-good%20good%20study%2C%20day%20day%20up-red.svg)](https://en.wikipedia.org/wiki/Day_Day_Up)

We will working on the Leetcode questions! Unit tests are recommended.

### Questions table
| question      | unit test      | Runtime beat   | Author        |
| Remove Duplicates from Sorted Array |:161 cases: |:54.77%: | Cory:|


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
