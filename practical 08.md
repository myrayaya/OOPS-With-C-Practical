## Program - 8: Create a Matrix class. Write a menu-driven program to perform following Matrix operations (exceptions should be thrown by the functions if matrices passed to them are incompatible and handled by the main() function): 

a. Sum 

b. Product 

c. Transpose

- Input Code:-
```
#include <iostream>
using namespace std;

class Matrix
{
    int mat[3][3];

public:
    void input()
    {
        cout << "Enter the matrix (3x3): \n";
        for (int i = 0; i < 3; i++)
            for (int j = 0; j < 3; j++)
                cin >> mat[i][j];
    }

    void display()
    {
        for (int i = 0; i < 3; i++)
        {
            for (int j = 0; j < 3; j++)
                cout << mat[i][j] << " ";
            cout << endl;
        }
    }


    Matrix operator+(Matrix m)
    {
        Matrix res;
        for (int i = 0; i < 3; i++)
            for (int j = 0; j < 3; j++)
                res.mat[i][j] = mat[i][j] + m.mat[i][j];
        return res;
    }

    Matrix operator*(Matrix m)
    {
        Matrix res;
        for (int i = 0; i < 3; i++)
            for (int j = 0; j < 3; j++)
            {
                res.mat[i][j] = 0;
                for (int k = 0; k < 3; k++)
                    res.mat[i][j] += mat[i][k] * m.mat[k][j];
            }
        return res;
    }

    Matrix transpose()
    {
        Matrix res;
        for (int i = 0; i < 3; i++)
            for (int j = 0; j < 3; j++)
                res.mat[i][j] = mat[j][i];
        return res;
    }
};

int main()
{
    Matrix A, B, C;
    int choice;

    A.input();
    B.input();

    do
    {
        cout << "\n Menu: \n1. Sum \n2. Product \n3. Transpose \n4. Exit \nEnter your choice: ";
        cin >> choice;

        switch (choice)
        {
            case 1:
                C = A + B;
                C.display();
                break;
            case 2:
                C = A * B;
                C.display();
                break;
            case 3:
                C = A.transpose();
                C.display();
                break;
            case 4:
                cout << "Exiting... \n";
                break;
            default:
                cout << "Invalid choice! ";
        }
    } while (choice != 4);

    return 0;
}
```

- Output:-

![image](https://github.com/user-attachments/assets/ed001f49-938a-48a8-b667-3b7b1f8267fc)

![image](https://github.com/user-attachments/assets/137d5e71-05d4-4ae8-b5f3-f39aab2e8dfc)
