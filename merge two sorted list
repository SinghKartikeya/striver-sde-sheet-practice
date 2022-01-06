# striver-sde-sheet-practice
Merge Two Sorted Lists
c++

****************

class Solution {
public:
    ListNode* mergeTwoLists(ListNode* list1, ListNode* list2) {
        if(list1==NULL)
            return list2;
        if(list2==NULL)
            return list1;
        ListNode *fina;
        if(list1->val < list2->val)
        {
            fina=list1;
            fina->next=mergeTwoLists(list1->next,list2);
                
        }
        else
        {
            fina=list2;
             fina->next=mergeTwoLists(list1,list2->next);
        }
        
        
        return fina;
    }
    
    };
