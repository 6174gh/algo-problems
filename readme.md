# Problems

## 1. Huffman Coding Algorithm

> Greedy -

1. Logic

```
Every alphabet uses 8 bits and some are repeated more frequenty.This algorithm assign small binary codes to more 
frequent alphabets thus reducing the size of total file.
```

2. Algorithm

```
1: Find character frequencies
2: Make a binary tree for each charcter which contains itself and its frquency.
3: Find two characters with minimum frequencies
4: Add their frequencies
5: Create new node and store sum of frequencies from step 4
6. Add least frequency node to left and other one to right
7. Repeat step 3-6 until there is only one tree
8: Now traverse the tree from root to leaf
9: Assign 0 to path to left subtree and 1 to right subtree
10: To obatin binarycode for a character traverse from root to the leaft node contating charcter while tracing the bits along the path
11: New Binary code table is formed by repeating step 10 for all chracters

Note:
    One code cannot be prefix of any other code.
    To check if it worked correct check if  all leaf nodes are charcters.
    Time Complexity: O(nlog(n))
```

3. Use Cases / Benefits

```
1: On average saves 10-30 % size of file.
```

