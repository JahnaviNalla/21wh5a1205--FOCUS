
class Solution:
    def maxProfit(self, prices: List[int]) -> int:
        l = 0
        r = 1
        p =0
        while(r < len(prices)):
            curprofit = prices[r] - prices[l]
            if(prices[r] > prices[l]):
                p = max(curprofit,p)
            else:
                l = r
            r +=1
        return p
