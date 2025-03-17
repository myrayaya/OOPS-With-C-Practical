## Program 12: Find if a number is prime or not. And if, number is less than 1, show error.

- Input Code:-
```
#include <iostream>
#include <stdexcept>
using namespace std;

class PrimeException : public exception {
public:
    const char* what() const throw() {
        return "Number must be greater than 1!";
    }
};

/* Function to check if the number is prime */
bool isPrime(int num) {
    if (num < 2)
        throw PrimeException();

    for (int i = 2; i * i <= num; i++) {
        if (num % i == 0)
            return false;
    }
    return true;
}

int main()
{
    int num;
    cout << "Enter a number: ";
    cin >> num;

    try {
        if (isPrime(num))
            cout << num << "is a prime number. \n";
        else
            cout <<  num << "is not a prime number. \n";
    } catch (PrimeException& e) {
        cout << "Error: " << e.what() << endl;
    }

    return 0;
}
```

- Output:-

![image](https://github.com/user-attachments/assets/d760cc74-c70b-4b6e-aa35-9ea5d094989b)

![image](https://github.com/user-attachments/assets/99d0d24f-bebe-4d14-8807-7becb0ea7915)

![image](https://github.com/user-attachments/assets/cbb42181-7ed3-4c22-be77-33f2e5162180)
