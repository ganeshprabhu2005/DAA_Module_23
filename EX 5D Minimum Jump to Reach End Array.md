# EX 5D Minimum Jump to Reach End Array
## DATE:16-08-2025
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm

1. Input the size of the array `n`.
2. Read `n` integers into array `arr`.
3. Define a recursive function `minJumps(arr, l, h)` to compute the minimum jumps from index `l` to index `h`.
4. Base Case 1: If `l == h`, return 0 (already at the destination).
5. Base Case 2: If `arr[l] == 0`, return infinity (can't move forward from current position).
6. Initialize `min` to infinity to track the minimum number of jumps.
7. Loop through indices `i` from `l+1` to `h`:
   * Check if `i` is reachable from `l` (i.e., `i < l + arr[l] + 1`).
   * Recursively calculate `jumps = minJumps(arr, i, h)`.
   * If `jumps` is valid (not infinity) and `jumps + 1 < min`, update `min = jumps + 1`.
8. After the loop, return `min` as the minimum number of jumps from `l` to `h`.
9. In `main`, call `minJumps(arr, 0, n-1)` to compute the result from start to end.
10. Output the result as the minimum number of jumps to reach the end of the array.

## Program:
```
To implement the program to finding the minimum number of jumps needed to reach end of the array.
Developed by: GANESH PRABHU J
Register Number: 212223220023
```
```PY
def minJumps(arr, l, h):
    if (h == l):
        return 0
    if (arr[l] == 0):
        return float('inf')
    min = float('inf')
    for i in range(l + 1, h + 1):
        if (i < l + arr[l] + 1):
            jumps = minJumps(arr, i, h)
            if (jumps != float('inf') and
                       jumps + 1 < min):
                min = jumps + 1
 
    return min
arr = []#[1, 3, 6, 3, 2, 3, 6, 8, 9, 5]
n = int(input()) #len(arr)
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr, 0, n-1))
 
```
## Output:

![image](https://github.com/user-attachments/assets/4f44a9a0-723f-4e79-9900-c77f4586cb7e)


## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
