# Cryptography

- Cryptography comes from Crypto + graphy which means a secret text

- the process of making text secret is called encryption and the reverse is decryption

- it is used to send share or connect between users in order to protect their privacy

- there are many ways used such as the exchange table where the message is being divided then placed in a table of columns then took the columns and formed a words of the same size and could be done multiply times.


## Caesar cipher

- In cryptography, a Caesar cipher, also known as Caesar's cipher, the shift cipher, Caesar's code or Caesar shift is one of the simplest and most widely known encryption techniques

- Example:

- The transformation can be represented by aligning two alphabets; the cipher alphabet is the plain alphabet rotated left or right by some number of positions. For instance, here is a Caesar cipher using a left rotation of three places, equivalent to a right shift of 23 (the shift parameter is used as the key):

Plain:    ABCDEFGHIJKLMNOPQRSTUVWXYZ
Cipher:   XYZABCDEFGHIJKLMNOPQRSTUVW

- When encrypting, a person looks up each letter of the message in the "plain" line and writes down the corresponding letter in the "cipher" line.

Plaintext:  THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG
Ciphertext: QEB NRFZH YOLTK CLU GRJMP LSBO QEB IXWV ALD

Deciphering is done in reverse, with a right shift of 3.

## How to break the Cipher

- The Caesar cipher can be easily broken even in a ciphertext-only scenario. Two situations can be considered:

1. an attacker knows (or guesses) that some sort of simple substitution cipher has been used, but not specifically that it is a Caesar scheme.
2. an attacker knows that a Caesar cipher is in use, but does not know the shift value.

- In the first case, the cipher can be broken using the same techniques as for a general simple substitution cipher, such as frequency analysis or pattern words , While solving, it is likely that an attacker will quickly notice the regularity in the solution and deduce that a Caesar cipher is the specific algorithm employed.
- In the second instance, breaking the scheme is even more straightforward. Since there are only a limited number of possible shifts (25 in English), they can each be tested in turn in a brute force attack.One way to do this is to write out a snippet of the cipher text in a table of all possible shifts– a technique sometimes known as **"completing the plain component"**.

