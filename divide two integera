class Solution {
    public int divide(int dividend, int divisor) {
        if (dividend == -(1 << 31) && divisor == -1) {
            return Integer.MAX_VALUE;
        }
        
        boolean isPositive = ((dividend > 0 && divisor > 0)
                             || (dividend < 0 && divisor < 0));
        
        long a = Math.abs((long) dividend);
        long b = Math.abs((long) divisor);
        
        int quotient = 0;
        
        if (a == b) {
            return isPositive ? 1 : -1;
        }
        
        //a = 100
        // b = 3
        while (a >= b) {
            int i = 0;
            while ((b << i) <= a) {
                i++;
            }
            
            quotient += (1 << (i - 1));
            a -= (b << (i - 1));
        }
        
        return isPositive ? quotient : -quotient;
    }
}
