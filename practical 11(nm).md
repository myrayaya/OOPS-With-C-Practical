## Program 11: Check if the exception is printed with certain condition.

- Input Code:-
```
#include <iostream>
#include <stdexcept>
using namespace std;

class MatrixException : public exception {
public:
    const char* what() const throw(){
        return "Matrix Dimensions are incomparable! ";
    }
};

void checkCompatability(int rows1, int cols1, int rows2, int cols2) {
    if (cols1 != rows2)
        throw MatrixException();
}

int main()
{
    try {
        checkCompatability(3, 7, 5, 8);
    } catch (MatrixException& e) {
        cout << "Error: " << e.what() << endl;
    }
    return 0;
}
```

- Output:-

![image](https://github.com/user-attachments/assets/678885e3-c117-48fc-b490-0c6bed079fd2)

