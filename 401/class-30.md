# Read 30: Hash Tables

* [Read Intro to Hash Tables](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)
  * A good hash map size is 1024.
  * If there are collisions it stores linked list nodes in the array location
  * To store values, hash tables:

    1. accept a key
    2. calculate the hash of the key
    3. use modulus to convert the hash into an array index
    4. store the key with the value by appending both to the end of a linked list

  * To read values, hash maps:

    1. accept a key
    2. calculate the hash of the key
    3. use modulus to convert the hash into an array index
    4. use the array index to access the short LinkedList representing a bucket
    5. search through the bucket looking for a node with a key/value pair that matches the key you were given

* [Watch what is a hash table?](https://www.youtube.com/watch?v=MfhjkfocRR0&ab_channel=PaulProgramming)

* [Read basics of hash tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)

* [Skim hash table wiki](https://en.wikipedia.org/wiki/Hash_table)
