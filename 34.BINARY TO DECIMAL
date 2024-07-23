#include <stdio.h>
int binaryToDecimal(int n);
int main() {
    int n;
    printf("Enter a binary number: ");
    scanf("%d", &n);
    printf("The decimal equivalent is: %d\n", binaryToDecimal(n));
    return 0;
}
int binaryToDecimal(int n) {
    int decimal = 0, base = 1, remainder;
     while (n > 0) 
	 {
        remainder = n % 10;
        decimal += remainder * base;
        n /= 10;
        base *= 2;
    }
     return decimal;
}
