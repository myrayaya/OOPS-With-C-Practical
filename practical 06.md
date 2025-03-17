## Program 6: Write a program to search a given element in a set of N numbers using Binary search:- 

(i) with recursion 

(ii) without recursion. 

- Input Code:-
```
#include <iostream>
#include <vector>
using namespace std;

/* Recursive Binary Search */
int binarySearchRecursive(vector<int>& arr, int left, int right, int key)
{
    if (left > right) return -1;
    int mid = left + (right - left) / 2;

    if (arr[mid] == key) return mid;
    if (arr[mid] > key) return binarySearchRecursive(arr, left, mid - 1, key);
    return binarySearchRecursive(arr, mid + 1, right, key);
}

/* Iterative Binary Search */
int binarySearchIterative(vector<int>& arr, int key)
{
    int left = 0, right = arr.size() - 1;
    while (left <= right)
    {
        int mid = left + (right - left) / 2;
        if (arr[mid] == key) return mid;
        if (arr[mid] > key) right = mid - 1;
        else left = mid + 1;
    }
    return -1;
}

int main()
{
    vector<int> arr = {1, 3, 5, 7, 9, 11, 13};
    int key = 9;

    /* Recursive Search */
    int indexRec =  binarySearchRecursive(arr, 0, arr.size() - 1, key);
    cout << "Recursive Binary Search: " << (indexRec != -1 ? "Found at index " + to_string(indexRec) : "Not Found") << endl;

    /* Iterative Search */
    int indexIter = binarySearchIterative(arr, key);
    cout << "Iterative Binary Search: " << (indexIter != -1 ? "Found at index " + to_string(indexIter) : "Not Found") << endl;

    return 0;
}
```

- Output:-

![image](https://github.com/user-attachments/assets/5aff6b6b-d074-48bb-8403-9f76ee102132)
