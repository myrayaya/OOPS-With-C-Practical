## Write a program that prints a table indicating the number of occurrences of each 
alphabet in the text entered as command line arguments. 
- Input Code:-
```
#include <iostream>
#include <string>
#include <map>
using namespace std;

void countOccurences(string str)
{
    map<char, int> freq;

    for (char c : str)
    {
        if (isalpha(c)) { /* Consider only alphabets */
            freq[tolower(c)]++;
        }
    }

    cout << "Character Frequency Table: \n";
    for (auto pair : freq) {
        cout << pair.first << " -> " << pair.second << endl;
    }
}

int main()
{
    string input;
    cout << "Enter a string: ";
    getline(cin, input);

    countOccurences(input);

    return 0;
}
```

- Output:-

![image](https://github.com/user-attachments/assets/f622fa5e-03e9-4f42-a751-db823c8e3484)
