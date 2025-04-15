# blind-13-75
Counting bits


A good follow up program to No . of 1 bits program .

Here brute force approach O(n log n).

n+1 size array -> for each number log n bits are required. 

And we check bit by bit , for each number .


But more efficient approach would be utilise upon already calculated results.

i.e if n is odd, no.of set bits in n= no.of set bits in n/2 + 1 

   if n is even, no.of set bits in n = no.of set bits in n/2 


Initially result=[0]*(n+1)  -> list builder short hand notation

then , result[i] = result[i>>1] + 1, if i is odd , else result[i>>1]


More efficiently, result[i] = result[i>>1] + i&1

Using this analytical concept , we can build the list , as we iterate along.

Time complexity : O(n)

Space complexity : O(1)
