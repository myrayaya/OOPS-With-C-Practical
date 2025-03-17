## Program 13:  Create a class Student containing fields for Roll No., Name, Class, Year and Total Marks. Write a program to store 5 objects of Student class in a file. Retrieve these records from the file and display them. 

- Input Code:-
```
#include <iostream>
using namespace std;

class Student {
public:
    int rollNo;
    string name;
    string className;
    int year;
    float totalMarks;

    void input() {
        cout << "Enter Roll No, Name, Class, Year, and Total Marks: ";
        cin >> rollNo >> name >> className >> year >> totalMarks;
    }

    void display() {
        cout << "Roll No: " << rollNo << ", Name: " << name
             << ", Class: " << className << ", Year: " << year
             << ", Total Marks: " << totalMarks << endl;
    }
};

int main()
{
    Student students[4];

    /* Taking input for 4 Students */
    for (int i = 0; i < 4; i++) {
        cout << "Enter Student Details: " << i + 1 << ": \n";
        students[i].input();
    }

    cout << "\nStudent Details: \n";
    for (int i = 0; i < 4; i++) {
        students[i].display();
    }

    return 0;
}
```

- Output:-

![image](https://github.com/user-attachments/assets/6b180a28-a63c-4dd8-9804-89729465df5c)
