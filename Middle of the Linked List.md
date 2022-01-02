# striver-sde-sheet-practice
Middle of the Linked List
c++ code

*******

/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode() : val(0), next(nullptr) {}
 *     ListNode(int x) : val(x), next(nullptr) {}
 *     ListNode(int x, ListNode *next) : val(x), next(next) {}
 * };
 */
class Solution {
public:
    ListNode* middleNode(ListNode* head) {
        
        ListNode *m = head;
        
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
