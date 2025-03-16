## Write a menu driven program to perform string manipulation (without using inbuilt string functions):
a. Show address of each character in string 

b. Concatenate two strings. 

c. Compare two strings 

d. Calculate length of the string (use pointers) 

e. Convert all lowercase characters to uppercase 

f. Reverse the string 

g. Insert a string in another string at a user specified position

- Input Code:-
```
#include <iostream>
#include <cstring> /* For strlen() */
using namespace std;

/* Function to display ASCII Values */
void displayASCII(string str)
{
    cout << "ASCII Values: \n";
    for (char c : str)
    {
        cout << c << " -> "<< int(c) << endl;
    }
}

/* Function to concatenate two strings (without in-built functions) */
void concatenateStrings(char str1[], char str2[])
{
    int i = strlen(str1), j = 0;
    while (str2[j] != '\0') 
    {
        str1[i] = str2[j];
        i++; j++;
    }
    str1[i] = '\0';
}

/* Function to compare two strings */
bool compareStrings(char str1[], char str2[])
{
    int i = 0;
    while (str1[i] != '\0' && str2[i] != '\0') 
    {
        if (str1[i] != str2[i])
            return false;
        i++;
    }
    return str1[i] == str2[i]; /* Ensure both end at the same position */
}

/* Function to find string length using pointers */
int stringLength(char* str)
{
    int len = 0;
    while (*str != '\0') 
    {
        len++;
        str++;
    }
    return len;
}

/* Function to convert lowercase to uppercase */
void toUppercase(char str[])
{
    int i = 0;
    while (str[i] != '\0')
    {
        if (str[i] >= 'a' && str[i] <='z')
        {
            str[i] -= 32;
        }
        i++;
    }
}

/* Function to create reverse of a string */
void reverseString(char str[])
{
    int len = stringLength(str);
    for (int i = 0; i < len / 2; i++)
    {
        swap(str[i], str[len - i - 1]);
    }
}

int main()
{
    char str1[100], str2[100];

    cout << "Enter first string: ";
    cin >> str1;
    cout << "Enter second string: ";
    cin >> str2;

    /* using function to show address of each character in a string */
    displayASCII(str1);

    /* using function to show concatenation of two strings */
    concatenateStrings(str1, str2);
    cout << "Concatenated String: " << str1 << endl;

    /* using function to show comparison of twp strings */
    cout << "String are " << (compareStrings(str1, str2) ? "equal" : "not equal") << endl;

    /* using function to show the length of the string */
    cout << "Length of first string: " << stringLength(str1) << endl;

    /* using function to show conversion of string to uppercase */
    toUppercase(str1);
    cout << "Uppercase String: " << str1 << endl;

    /* using function to show reversal of the string */
    reverseString(str1);
    cout << "Reversed String: " << str1 << endl;

    return 0;
}
```

- Output:-

![image](https://github.com/user-attachments/assets/05e901c3-2183-40ca-be02-3b848c4a371c)
