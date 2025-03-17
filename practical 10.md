## Program 10: Create a Triangle class. Add exception handling statements to ensure the following conditions: all sides are greater than 0 and sum of any two sides are greater than the third side.  The class should also have overloaded functions for calculating the area of a right angled triangle as well as using Heron's formula to calculate the area of any type of triangle.

- Input Code:-
```
#include <iostream>
#include <cmath> /* For using Square Root sqrt */
using namespace std;

class Triangle{
public:
    /* Area with Base and Height */
    double area(double base, double height) {
        return 0.5 * base * height;
    }

    /* Area with 3 sides of the Triangle (Using Heron's formula) */
    double area(double a, double b, double c){
        double s = (a + b + c) / 2;
        return sqrt(s * (s - a) * (s - b) * (s - c));
    }
};

int main()
{
    Triangle t;
    cout << "Area (Base, Height): " << t.area(6, 12) << endl;
    cout << "Area (Three Sides): " << t.area(5, 12, 13) << endl;
}
```

- Output:-

![image](https://github.com/user-attachments/assets/03a9f799-3df4-45d7-b2cf-074f844e2ed1)
