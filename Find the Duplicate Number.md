# striver-sde-sheet-practice
Find the Duplicate Number
c++

********************

class Solution {
public:
    int findDuplicate(vector<int>& nums) {
        
        sort(nums.begin(),nums.end());
        int i,c=0;
        for(i=0;i<nums.size();i++)
        {
            if(nums[i]==nums[i+1])
            {
                c=i;
            break;
            }
        }
        
            return nums[c];
        
    }
    
};
