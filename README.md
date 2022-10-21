# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:

## Linear Search:
1.	Start from the leftmost element of array[] 
2.	Compare k with each element of array[] one by one.
3.	If k matches with an element in array[] , return the index.
4.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. 
5.	This is done by setting low to low = mid + 1.
6.	Else, compare x with the middle element of the elements on the left side of mid. 
7.	This is done by setting high to high = mid - 1.
8.	Repeat steps 2 to 5 until low meets high.

## Program:
i)	#Use a linear search method to match the item in a list.
``` python
''' 
Program for linear search method to match the item in a list
Developed by: SIVA CHANDRAN R
RegisterNumber: 22005531
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if array[i]==k:
            return i
    return -1
array = eval(input())
k = eval(input())
n=len(array)
array.sort()
result=linearSearch(array,n,k)
if result!=-1:
    print(array)
    print("Element found at index: ",result)
else:
    print(array)
    print("Element not found")

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
``` python
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: SIVA CHANDRAN R
RegisterNumber: 22005531
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high - low)//2
        
        if array[mid]==k:
            return mid
            
        elif array[mid]<k:
            low=mid + 1
        else:
            high=mid+1
    return -1
            
array = eval(input())
array.sort()
k = eval(input())
result=binarySearchIter(array,k,0,len(array)-1)
if result!=-1:
    print(array)
    print("Element found at index: ",result)
else:
    print(array)
    print("Element not found")

```
iii)	# Find the element in a list using Binary Search (recursive Method).
``` python
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: SIVA CHANDRAN R
RegisterNumber: 220005531
'''
def binarySearchIter(array, k, low, high):
    while high>=low:
        mid=low+(high - low)//2
        
        if array[mid]==k:
            return mid
            
        elif array[mid]>k:
            return binarySearchIter(array,k,low,mid-1)
        else:
            return binarySearchIter(array,k,mid+1,high)
    else:
        return -1
            
array = eval(input())
array.sort()
n=len(array)
k = eval(input())
array.sort()
result=binarySearchIter(array,k,0,n-1)
if result!=-1:
    print(array)
    print("Element found at index: ",result)
else:
    print(array)
    print("Element not found",)
    
    
    
    
    
    
```
## Sample Input and Output
![OUTPUT](out5.png)

![OUTPUT](out7.png)

![OUTPUT](out8.png)






## Result
Thus the linear search and binary search algorithm is implemented using python programming.
