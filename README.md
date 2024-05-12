# EXP-7 Linear Search and Binary search
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
DEVELOPED BY:SHIVAA PALANIYAPPAN V
REGISTER NUMBER:212223110050
i)	#Use a linear search method to match the item in a list.
```
def search(arr,key,n):
    for i in range(0,n):
        if key==arr[i]:
            return (f"Element found at index:  {i}")
    if key not in arr:
        return ("Element not found")

arr=eval(input())
key = int(input())
n=len(arr)
arr.sort()
print(arr)
print(search(arr,key,n))


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```

def binary(arr,key,low,high):
    while(low<=high):
        mid = low+(high-low)//2
        if arr[mid]==key:
            return mid
        elif arr[mid]<key:
            low = mid +1
        elif arr[mid]>key:
            high=mid-1
    return -1
arr=eval(input())
key=int(input())
arr.sort()
low,high=0,len(arr)-1
print(arr)
result = binary(arr,key,low,high)
if result ==-1:
    print("Element not found")
else:
    print(f"Element found at index:  {result}")



```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
def binary(arr,key,low,high):
    if high>=low:
        mid = low+(high-low)//2
        if arr[mid]==key:
            return mid
        elif arr[mid]<key:
            return binary(arr,key,mid+1,high)
        elif arr[mid]>key:
            return binary(arr,key,low,mid-1)
    return -1
    
arr=eval(input())
key=int(input())
arr.sort()
low,high=0,len(arr)-1
print(arr)
result = binary(arr,key,low,high)
if result ==-1:
    print("Element not found")
else:
    print(f"Element found at index:  {result}")




```
## Sample Input and Output

## LINEAR SEARCH
![image](https://github.com/shivaa-palaniyappan/Search-Algorithms/assets/146915611/a14692af-7634-4663-8edf-3bc95156214e)
## BINARY SEARCH (USING ITERATIVE METHOD)
![image](https://github.com/shivaa-palaniyappan/Search-Algorithms/assets/146915611/6fa0cf53-a3e0-4091-aedf-aed42474ecaf)
## BINARY SEARCH (USING RECURSIVE METHOD)
![image](https://github.com/shivaa-palaniyappan/Search-Algorithms/assets/146915611/aa49abae-d475-44be-aa43-4399ff7023b5)




## Result
Thus the linear search and binary search algorithm is implemented using python programming.
