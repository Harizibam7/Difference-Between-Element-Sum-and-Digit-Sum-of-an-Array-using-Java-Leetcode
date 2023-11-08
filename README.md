# Difference-Between-Element-Sum-and-Digit-Sum-of-an-Array-using-Java-Leetcode
    class Solution {
        public int digitsum(int n){
            int sum =0;
            int temp;
            while(n>0){
                temp =n%10;
                sum = sum + temp;
                n = n/10;
            }
            return sum;
        }
        public int differenceOfSum(int[] nums) {
            int elementSum =0;
            int digitSum =0;
            for(int i =0; i<nums.length;i++){
                elementSum+=nums[i];
                digitSum+=digitsum(nums[i]);
            }
            int result = elementSum  - digitSum;    
    
            return result;
        }
    }
