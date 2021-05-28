# Hash Table

**Resources:**
- [Data Structure and Algorithms - Hash Table](https://www.tutorialspoint.com/data_structures_algorithms/hash_data_structure.htm)
- [Hash Table](https://www.interviewcake.com/concept/java/hash-map)

## What is Hash Table? 

**Hash Table** is a data structure which stores data in an associative manner. In a hash table, data is stored in an array format, where each data value has its own unique index value. Access of data becomes very fast if we know the index of the desired data.

**Hashing** is a technique to convert a range of key values into a range of indexes of an array.

## Basic Operations

1. Search 
    - Searches an element in a hash table.

2. Insert
    - inserts an element in a hash table.

3. Delete 
    - Deletes an element from a hash table.

## Strengths & Weaknesses

**Strengths:**

1. **Fast lookups** 
    - Lookups take O(1)O(1) time on average.
2. **Flexible keys** 
    - Most data types can be used for keys, as long as they're hashable.

**Weaknesses:**

1. **Slow worst-case lookups** 
    - Lookups take O(n)O(n) time in the worst case.
2. **Unordered** 
    - Keys aren't stored in a special order. If you're looking for the smallest key, the largest key, or all the keys in a range, you'll need to look through every key to find it.
3. **Single-directional lookups** 
    - While you can look up the value for a given key in O(1)O(1) time, looking up the keys for a given value requires looping through the whole dataset—O(n)O(n) time.
4.** Not cache-friendly** 
    - Many hash table implementations use linked lists, which don't put data next to each other in memory.

## Real life examples

**Some examples of how hashing is used in our lives include:**

1. In universities, each student is assigned a unique roll number that can be used to retrieve information about them.
2. In libraries, each book is assigned a unique number that can be used to determine information about the book, such as its exact position in the library or the users it has been issued to etc.

>In both these examples the students and books were hashed to a unique number.