# Hashtables

## What is a Hashtable

**Hash:** A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

**Buckets:** A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
**Collisions:** A collision is what happens when more than one key gets hashed to the same location of the hashtable.

**Why do we use them:**
Hold unique values - Dictionary - Library


	
## Structure
### Hashing
a hash code turns a key into an integer. It’s very important that hash codes are deterministic: their output is determined only by their input.

### Creating a Hash
- A hashtable traditionally is created from an array. I always like the size 1024. this is important for index placement. After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a possible suggestion:
1. Add or multiply all the ASCII values together.
2. Multiply it by a prime number such as 599.
3. Use modulo to get the remainder of the result, when divided by the total size of the array.
4. Insert into the array at that index.
Example:

        Key = "Cat"
        Value = "Josie"
        67 + 97 + 116 = 280
        280 * 599 = 69648
        69648 % 1024 = 16
        Key gets placed in index of 16. 


## Internal Methods
**Add()**
When adding a new key/value pair to a hashtable:
- send the key to the GetHash method.
- Once you determine the index of where it should be placed, go to that index
- Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
- If something does exist, add the new key/value pair to the data structure within that bucket.

**Find()**
The Find takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

**Contains()**
The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.

**GetHash()**
The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.
