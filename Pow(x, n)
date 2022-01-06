# striver-sde-sheet-practice
Pow(x, n)
c++

********************

class Solution {
public:
    double myPow(double x, int n) {
  if(n < 0){
			n++;
			return 1/x * myPow(1/x, -n);
		}
        else if(n>0)
        {
            if(n==1)  return x;
            if(n%2) return x*myPow(x*x,n/2);
            else return myPow(x*x,n/2);
        }
        else if(n==0) return 1;
        return x;
    }
    
    
};
