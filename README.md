# print-string
You are given a sequence of 26 integers P=(P1, P2, …, P26 ) consisting of integers from 1 to 26. It is guaranteed that all elements in P are distinct. Print a string S of length 26 that satisfies the following condition. For every i (1 ≤ i ≤ 26), the i- th character of S is the lowercase English letter that comes Pi- th in alphabetical order. 

def print_string(sequence):
    chars = [''] * 26
    
    for i, val in enumerate(sequence):
        char = chr(val + ord('a') - 1)
        chars[i] = char
    
    return ''.join(chars)

# input
sequence = list(map(int, input().split()))

# Output 
print(print_string(sequence))
