# **Read: Hash Tables**
#### a hash table, also known as hash map, is a data structure that implements a set abstract data type, a structure that can map keys to values. A hash table uses a hash function to compute an index, also called a hash code, into an array of buckets or slots, from which the desired value can be found. During lookup, the key is hashed and the resulting hash indicates where the corresponding value is stored.

![](https://media.geeksforgeeks.org/wp-content/uploads/chain-hashing-1.png)

<br>

### What is a Hashtable?
* Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
* Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
* Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

### Why do we use them?
* Hold unique values
* Dictionary
* Library


## How to Create a Hash?
1- Add or multiply all the ASCII values together.
2- Multiply it by a prime number such as 599.
3- Use modulo to get the remainder of the result, when divided by the total size of the array.
4- Insert into the array at that index.

Example:

```
Key = "Cat"
Value = "Josie"

67 + 97 + 116 = 280

280 * 599 = 69648

69648 % 1024 = 16

Key gets placed in index of 16. 
```

<br>

# How to avoid the Collisions?
### Collisions are solved by changing the initial state of the buckets. Instead of starting them all as null we can initialize a LinkedList in each one! Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list. Each index in the array is called a “bucket” because it can store multiple key/value pairs.
