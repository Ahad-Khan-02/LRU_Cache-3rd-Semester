# LRU_Cache-3rd-Semester
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## LRU Cache Implementation:
This document describes an implementation of a Least Recently Used (LRU) Cache using Python. The cache is built using a doubly linked list and a dictionary (hash map) to achieve efficient O(1) time complexity for get and put operations.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Features:
Capacity Control: Allows setting a maximum capacity for the cache (0–50).
LRU Eviction Policy: Automatically removes the least recently used item when the cache exceeds capacity.
Miss Rate Calculation: Tracks the cache's miss rate as a percentage.
Valid Range Check: Ensures keys and values fall within a valid range (0–100).

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Class Overview

### Node
A helper class for representing nodes in the doubly linked list.

  Attributes:
   -key: The key of the node.
   -val: The value of the node.
   -prev, next: Pointers to the previous and next nodes in the list.

### LRU_Cache
Main class implementing the LRU Cache functionality.

## Methods:
### __init__(cap)
Initializes the cache with a given capacity.
Ensures capacity is between 0 and 50.

### get(key)
Retrieves the value for the given key.
Moves the node to the most recently used (MRU) position if found.
Returns -1 if the key is not in the cache.

### put(key, val)
Adds or updates a key-value pair in the cache.
Moves the key to the MRU position.
Evicts the least recently used (LRU) item if the cache exceeds capacity.

### calc_miss_rate()
Calculates and returns the cache miss rate as a percentage.

### print_cache()
Prints the current state of the cache in {key, value} format.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
