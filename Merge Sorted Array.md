# striver-sde-sheet-practice
Merge Sorted Array
c++

******************* 

class Solution {
public:
    void merge(vector<int>& nums1, int m, vector<int>& nums2, int n) {
        int k=m+n;
        int l=0;
        for(int i=0;i<k;i++)
        {
            if(i<m)
            nums1[i]=nums1[i];
        else
        {
            nums1[i]=nums2[l];
            l++;
        }
        }
        sort(nums1.begin(),nums1.end());
    }
};
