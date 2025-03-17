## Program 14: Copy the contents of one text file to another file, after removing all whitespaces.

- Input Code:-
```
#include <iostream>
#include <fstream>
using namespace std;

void removeWhitespace(string inputFile, string outputFile) {
    ifstream in(inputFile);
    ofstream out(outputFile);

    if (!in || !out) {
        cout << "Error opening the file! " << endl;
        return;
    }

    char ch;
    while (in.get(ch)) {
        if (!isspace(ch))
            out.put(ch);
    }

    cout <<"File copied successfully without whitespaces! \n";
    in.close();
    out.close();
}

int main()
{
    string inputFile = "input.txt";
    string outputFile = "output.txt";

    removeWhitespace(inputFile, outputFile);

    return 0;
}
```

- Output:-

![image](https://github.com/user-attachments/assets/aa56887e-1749-4dce-9861-2bc4a3f1af83)

![image](https://github.com/user-attachments/assets/bb3654f4-19c1-48a5-a33a-84deeaf95305)

![image](https://github.com/user-attachments/assets/a8d41f4b-496c-4307-b9a8-d04e13db1337)
