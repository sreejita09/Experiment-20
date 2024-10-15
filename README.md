## EXPERIMENT 20

## AIM:

To study and implement Sorting Algorithm
1. Selection sort
2. Insertion sort
3. Bubble sort

## THEORY:

In C++, sorting refers to the process of arranging elements in a specific order, typically in ascending or descending order. Sorting algorithms can be applied to arrays, vectors, or other containers to reorder the elements based on their values.<br>

1. *Selection Sort:*
* Selection Sort works by repeatedly finding the minimum element from the unsorted part of the array and swapping it with the first unsorted element.
* Time Complexity: O(n²) for all cases.
* Space Complexity: O(1) (in-place sorting). <br>
2. *Insertion Sort:*
* Insertion Sort works by building a sorted array one element at a time. It picks each element and inserts it into its correct position within the already sorted part of the array.
* Time Complexity: O(n²) in the worst case; O(n) in the best case (already sorted).
* Space Complexity: O(1) (in-place sorting). <br>
3. *Bubble Sort:*
* Bubble Sort repeatedly swaps adjacent elements if they are in the wrong order. The largest element "bubbles up" to its correct position after each pass.
* Time Complexity: O(n²) in the worst case.
* Space Complexity: O(1) (in-place sorting). <br>

~~~
#include <iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void s_sort(int *a, int elements) {
    int n = 0;
    int *b;

    while (n < elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}

int main() {
    int no_el;
    cout << "How many elements in your array?" << endl;
    cin >> no_el;
    int arr[no_el];

    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cin >> arr[i];
    }

    s_sort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    return 0;
}
~~~
![image](https://github.com/user-attachments/assets/30ac2f9c-1a1a-49ac-975c-56bd1dd99b12)

~~~
#include<iostream>
using namespace std;

void insertionSort(int arr[], int n) 
{
    for (int i = 1; i < n; i++) 
    {
        int key = arr[i];
        int j = i - 1;

        while (j >= 0 && arr[j] > key) 
        {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}

int main() {
    int n;
    cout << "How many elements in your array?" << endl;
    cin >> n;
    
    int arr[n];
    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    insertionSort(arr, n);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    
    return 0;
}
~~~
![image](https://github.com/user-attachments/assets/b7e21769-f0be-4034-9860-94b4f4d061a3)

~~~
#include<iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void bubbleSort(int *a, int elements) {
    int n = 0;
    int *b;

    while (n < elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}

int main() {
    int no_el;
    cout << "How many elements in your array?" << endl;
    cin >> no_el;

    int arr[no_el];
    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cin >> arr[i];
    }

    bubbleSort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;

    return 0;
}
~~~
![image](https://github.com/user-attachments/assets/cf7b2c09-c137-4137-9fb3-69ad9ef4e113)
