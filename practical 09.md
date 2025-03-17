## Program 9: Define a class Person having name as a data member. Inherit two classes Student and Employee from Person. Student has additional attributes as course, marks and year and Employee has department and salary. Write display() method in all the three classes to display the corresponding attributes. Provide the necessary methods to show runtime polymorphism.

- Input Code:-
```
#include <iostream>
using namespace std;

class Person{
protected:
    string name;
    int age;
public:
    void input()
    {
        cout << "Enter Name and Age: ";
        cin >> name >> age;
    }
    void display()
    {
        cout << "Name: " << name << " Age: " << age << endl;
    }
};

class Student : public Person {
    string course;
public:
    void input()
    {
        Person :: input();
        cout << "Enter Course Name: ";
        cin >> course;
    }

    void dsiplay()
    {
        Person :: display();
        cout << "Course Name: " << course << endl;
    }
};

class Employee : public Person {
    int salary;
public:
    void input()
    {
        Person :: input();
        cout << "Enter Salary: ";
        cin >> salary;
    }
    void display()
    {
        Person :: input();
        cout << "Salary: " << salary << endl;
    }
};

int main ()
{
    Student s;
    Employee e;

    cout << "Enter Student Details: \n";
    s.input();

    cout << "Enter Employee Details: \n";
    e.input();

    cout << "\n Student Details: \n";
    s.display();

    cout << "\n Employee Details: \n ";
    e.display();
}
```

- Output:-

![image](https://github.com/user-attachments/assets/a2e4d7e7-a7e9-4e65-8fcb-bdc1ceb813ee)
