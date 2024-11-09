#include <stdio.h>
int main() {
    int num1, num2, result;
    char operator;
    
    printf("Enter first value: ");
    scanf("%d", &num1);
    
    printf("Enter second value: ");
    scanf("%d", &num2);
    
    printf("Enter your operator (+, -, *, /): ");
    scanf(" %c", &operator);  // Notice the space before %c to handle previous newline
    
    switch(operator) {
        case '+':
            result = num1 + num2;
            break;
        case '-':
            result = num1 - num2;
            break;
        case '*':
            result = num1 * num2;
            break;
        case '/':
            // Add check for division by zero
            if (num2 == 0) {
                printf("Error: Division by zero is not allowed.\n");
                return 1;  // Exit program with an error code
            }
            result = num1 / num2;
            break;
        default:
            printf("Invalid operator input!\n");
            return 1;  // Exit program with an error code
    }
    
    printf("Result: %d\n", result);  // Add the missing semicolon
    return 0;
}
