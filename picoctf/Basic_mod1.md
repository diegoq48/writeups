# DESCRIPCION:

We have come across a peculiar message circulating on the servers, and we believe we've cracked a decryption scheme for it. You can download the message [here](link-to-message). The message comprises a series of numbers:

387 248 131 272 373 221 161 110 91 359 390 50 225 184 223 137 225 327 42 179 220 365 

Following the challenge instructions, we are instructed to:

1. Take each provided number and calculate mod 37.
2. Map each obtained modulo to a character set, where:
    a. Positions 0-25 represent uppercase letters.
    b. Positions 26-35 represent decimal digits.
    c. Position 36 represents the underscore symbol (_).

Here is the corresponding dictionary: "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"

We can create a script to perform the modulo calculation for each number and add the result to an array, converting it to its corresponding character based on the dictionary.

With all this information, we can generate the script to decrypt the flag:

```python
#!/usr/bin/env python3

# Create an array with the numbers provided in the message
a = [387, 248, 131, 272, 373, 221, 161, 110, 91, 359, 390, 50, 225, 184, 223, 137, 225, 327, 42, 179, 220, 365]

# Build the dictionary according to the instructions
alph = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"

# Calculate the modulo for each number and its corresponding value in the dictionary
# Save the results in an array for printing the final result
b = [alph[i % 37] for i in a]
print("picoCTF{" + ''.join(b) + "}")
```

# FLAG:
picoCTF{R0UND_N_R0UND_B0D5F596}