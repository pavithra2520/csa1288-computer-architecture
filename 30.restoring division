#include <stdio.h>
int restoreDivide(int dividend, int divisor) {
    int quotient = 0;
    int remainder = 0;
    int bits = sizeof(int) * 8; 
    for (int i = bits - 1; i >= 0; i--) {
        remainder = (remainder << 1) | ((dividend >> i) & 1); 
       if (remainder >= divisor) {
            remainder -= divisor;
            quotient = (quotient << 1) | 1; 
        } else {
            quotient = quotient << 1; 
        }
    }
    return quotient;
}
int main() {
    int dividend, divisor;
    printf("Enter the dividend: ");
    scanf("%d", &dividend);
    printf("Enter the divisor: ");
    scanf("%d", &divisor);
    int result = restoreDivide(dividend, divisor);
    printf("Result of %d divided by %d using Restoring Division: %d\n", dividend, divisor, result);
    return 0;
}
