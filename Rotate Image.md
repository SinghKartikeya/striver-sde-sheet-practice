# striver-sde-sheet-practice

Rotate Image
c++

***********************

class Solution {
public:
    void rotate(vector<vector<int>>& matrix) {
        int n=matrix.size();
        
        int arr[n][n];
        for(int i=0;i<n;i++)
        {
            int x=0;
            for(int j=n-1;j>=0;j--)
            {
                int p=matrix[j][i];
                arr[i][x]=p;
                x++;
            }
        }
        for(int i=0;i<n;i++)
        {
            for(int j=0;j<n;j++)
            {
                matrix[i][j]=arr[i][j];
            }
        }
        
    }
};
