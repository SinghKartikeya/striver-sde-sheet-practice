# striver-sde-sheet-practice
Middle of the Linked List
c++

*******************

class Solution {
public:
    ListNode* middleNode(ListNode* head) {
        
        ListNode* m = head;
        
        int cnt = 0;
        int len = 0;
        
        while(head)
        {
            len++;
            if(len / 2 != cnt)
            {
                cnt++;
                m=m->next;
            }
            head = head->next;
        }
        return m;
    }
};
