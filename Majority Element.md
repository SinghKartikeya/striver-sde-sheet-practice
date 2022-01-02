# striver-sde-sheet-practice
Majority Element
c++

*******************

class Solution {
public:
    int majorityElement(vector<int>& nums) {
       sort(nums.begin(),nums.end());
        int c=1,k=0,i;
        int ans;
        double p=nums.size()/2;
        if(p<1.0)
            ans=nums[0];
        else
        {
        for( i=1;i<nums.size();i++)
        {
            if(nums[k]==nums[i])
            {
                c++;                          
            }
            else if(c>(nums.size()/2))
            {
                ans=nums[k];
                break;
            }
                else
                {
                    c=1;
                    k=i;
                }
            
            
        }if(c>(nums.size()/2))
            ans=nums[k];
            
        }
        return ans;
    }
};
