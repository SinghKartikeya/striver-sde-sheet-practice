# striver-sde-sheet-practice

Search a 2D Matrix
c++

*******************

class Solution {
public:
    bool searchMatrix(vector<vector<int>>& matrix, int target) {
        int k=0;
        int m=matrix.size();
        int n=matrix[0].size();
        for(int i=0;i<m;i++)
        {
            for(int j=0;j<n;j++)
            {
                if(matrix[i][j]==target)
                    k++;
               
            }
        }
        if(k>=1)
        return true;
        else
            return false;
        
    }
};
