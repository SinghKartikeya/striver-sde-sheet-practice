# striver-sde-sheet-practice
Merge Intervals

c++

**********************

class Solution {
public:
    vector<vector<int>> merge(vector<vector<int>>& intervals) {
        sort(intervals.begin(),intervals.end());
            stack<pair<int,int>> s;
        s.push({intervals[0][0],intervals[0][1]});
        for(int i=1;i<intervals.size();i++)
        {
            int st1=s.top().first;
            int end1=s.top().second;
            int st2=intervals[i][0];
            int end2=intervals[i][1];
            if(end1<st2)
                s.push({st2,end2});
                else
                {
                    s.pop();
                    end1=max(end1,end2);
                    s.push({st1,end1});
                }
        }
        
        stack<pair<int,int>> ans;
        while(!s.empty())
        {
            ans.push(s.top());
            s.pop();
        }
        vector<vector<int>> inter;
        
        while(!ans.empty())
        {
            inter.push_back({ans.top().first,ans.top().second});
            ans.pop();
        }
        
        return inter;
    }
};
