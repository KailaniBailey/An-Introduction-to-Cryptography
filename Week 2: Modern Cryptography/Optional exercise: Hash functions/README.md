# Optional exercise: Hash functions

In the previous step you learned about what hashing and hash collisions are. In this step you will get some practical experience of hash functions.

## Hash generator

1. Using the online hash generator, hash your name to see what hash value it produces.

Hash functions are weird because even two values that are similar will have vastly different outputs when they are hashed.

2. Change your name slightly by changing a letter to uppercase, or some other minor change. What hash value does it produce?
3. How many characters in the hash function are the same?

## Hash collisions

This next task is a bit of fun, but may take you a long time to find values. Give it a go but don't spend too much time on it.

A hash collision is when two different words hash to the same hash value. Of course hash collisions can happen but are very hard to find. Let's play a little game to see if we can find one, or to see if we can find two words that hash to almost the same hash value.

Try and find two hash values that have the most number of same characters starting from the right hand side of the hash value.

For example:

- "University of Leeds" has the hash value "647f9f9f941c87bbd0ea651f97608d007cda462e2e246704d70003c27ce3ea5a"
- "4" has the hash value                        "4b227777d4dd1fc61c6f884f48641d02b4d121d3fd328cb08b5531fcacdabf8a"

Both hash values end in the same letter "a", so they have 1 character the same.
