# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by:GOKHULRAJ V
RegisterNumber: 23004889
'''
def linearSearch(array,n,k):
    for i in range(n):
        if array[i]==k:
            return i
    return -1
array = eval(input())
array.sort()
k = eval(input()) # k-item to be seared for
n=len(array)
print(array)
result = linearSearch(array,n,k)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:GOKHULRAJ V
RegisterNumber: 212223230064
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array = eval(input())
array.sort()
k = eval(input()) #k-item to be searched
print(array)
result=binarySearchIter(array,k,0,len(array)-1)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: GOKHULRAJ V
RegisterNumber: 212223230064
'''
def BinarySearch(arr, k, low, high):
    # Write your code here for binary search using recursive method
    if high >= low:
        mid = low + (high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid] > k:
            return BinarySearch(arr, k, low, mid-1)
        else:
            return BinarySearch(arr, k, mid+1, high)
    else:
        return -1
    
arr = eval(input())
#sort the array
arr.sort()
k = eval(input()) # k is the element to be searched for
result = BinarySearch(arr, k, 0, len(arr)-1)
# use the binary search function to find the result
if result == -1:
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result




```
## Sample Input 

![Screenshot 2023-12-30 105439](https://github.com/Gokhulraj2005/Search-Algorithm/assets/138849253/2a1cbc4a-6376-493f-8894-16ffe2c88e36)
![Screenshot 2023-12-30 105449](https://github.com/Gokhulraj2005/Search-Algorithm/assets/138849253/2c4caedd-5628-4b71-b64e-24d428f7fabf)
![Screenshot 2023-12-30 105457](https://github.com/Gokhulraj2005/Search-Algorithm/assets/138849253/0ba5a0bc-971e-4592-b7ef-397b9c2f145c)

##  Output

![Screenshot 2023-12-30 105853](https://github.com/Gokhulraj2005/Search-Algorithm/assets/138849253/b6c4620a-661d-418f-aaec-f0d490087423)
![Screenshot 2023-12-30 110010](https://github.com/Gokhulraj2005/Search-Algorithm/assets/138849253/cf180c22-51a5-4cde-8efd-ee89e3a1cc05)

![Screenshot 2023-12-30 110131](https://github.com/Gokhulraj2005/Search-Algorithm/assets/138849253/2999d516-e6e4-4690-b813-beaa33551e10)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
