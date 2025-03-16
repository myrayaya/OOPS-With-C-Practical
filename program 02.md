# Program - 2: Write a program to remove the duplicates from an array
- Input Code:-
```
#include <iostream>
#include <vector>
#include <set>
using namespace std;

void removeDuplicates(vector<int>& arr) {
    set<int> uniqueElements(arr.begin(), arr.end());
    arr.assign(uniqueElements.begin(), uniqueElements.end());
}

int main()
{
    vector<int> arr = {1, 1, 2, 2, 2, 3, 4, 4, 4 ,5, 6, 6, 6};
    
    cout << " Initial Array: ";
    for (int num : arr) cout << num << " ";

    removeDuplicates(arr);

    cout << "\n Array after removing duplicates: ";
    for (int num : arr) cout << num << " ";

    return 0;
}
```
### Output:-
![image](https://github.com/user-attachments/assets/fb365eb6-88d2-44ed-9255-54f69fc4b002)
