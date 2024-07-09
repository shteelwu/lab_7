```c
#include <stdio.h>
#include <math.h>

int main() {
    double x1, y1, r1, x2, y2, r2;
    printf("Enter the coordinates of the circles (x1, y1, r1, x2, y2, r2): ");
    scanf("%lf %lf %lf %lf %lf %lf", &x1, &y1, &r1,&x2,&y2,&r2);

    double distance = sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2));
    
    
    int i;

    if (distance == 0 && r1 == r2) {
        i= -1;
    } else if (distance > r1 + r2 || distance < fabs(r1 - r2)) {
        i = 0;
    } else if (distance == r1 + r2 || distance == fabs(r1 - r2)) {
        i = 1;
    } else {
        i = 2;
    }

    printf("Number of intersection points: %d\n", i);
    
    return 0;
}
