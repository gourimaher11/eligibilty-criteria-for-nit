 
#include <stdio.h>
int main() {
    float marks;
    char category;

    printf("Enter your 12th percentage marks: ");
    scanf("%f", &marks);

    if (marks < 60) {
        printf("You are NOT eligible to take admission in NIT.\n");
        return 0;  // Exit program early since marks are too low
    }

    printf("Enter your category (1 for General, 2 for obc, 3 for sc/st): ");
    scanf(" %c", &category);

    if (category == '1' || category == '2') {
        if (marks >= 75) {
            printf("You are eligible to take admission in NIT.\n");
        } else {
            printf("You are NOT eligible to take admission in NIT.\n");
        }
    }
    else if (category == '3') {
        printf("You are eligible to take admission in NIT.\n");
    }
    else {
        printf("Invalid category.\n");
    }

    return 0;
}
