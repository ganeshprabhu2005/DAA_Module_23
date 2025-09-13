# EX 5C Kadane's Algorithm
## DATE:16-08-2025
## AIM:
To write a python program to find the maximum contiguous subarray.


## Algorithm

1. Input the size of the array `n`.
2. Read `n` elements into the array `a`.
3. Initialize `max_till_now` with the first element `a[0]`.
4. Initialize `max_ending` as 0 (this will track the current subarray sum).
5. Loop through each element in the array from index `0` to `size - 1`:
6. Add the current element `a[i]` to `max_ending`.
7. If `max_ending` becomes negative, reset it to 0 (discard the current subarray).
8. If `max_ending` is greater than `max_till_now`, update `max_till_now` with `max_ending`.
9. After the loop, return `max_till_now` as the result.
10. Output the maximum contiguous subarray sum.

## Program:
```
To implement the program to find the maximum contiguous subarray.
Developed by: GANESH PRABHU J
Register Number: 212223220023
```
```PY
def maxSubArraySum(a,size):

    max_till_now = a[0]
    max_ending = 0
    
    for i in range(0, size):
        max_ending = max_ending + a[i]
        if max_ending < 0:
            max_ending = 0
        
        
        elif (max_till_now < max_ending):
            max_till_now = max_ending
            
    return max_till_now
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
  
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```
## Output:



## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray..
