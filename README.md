# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
# Program:
```
import math

# Probabilities given
p = [0.30, 0.25, 0.20, 0.12, 0.08, 0.05]

# Corresponding Huffman/Shannon-Fano code lengths
lk = [2, 2, 2, 3, 4, 4]

n = len(p)

# Average Codeword Length
L = sum(p[k] * lk[k] for k in range(n))

# Entropy
hs = sum(p[k] * math.log(1 / p[k], 2) for k in range(n))
hs = round(hs, 3)

# Efficiency & Redundancy
eff = round(hs / L, 3)
red = round(1 - eff, 3)

# Variance of codeword length
var = sum(p[k] * (lk[k] - L) ** 2 for k in range(n))
var = round(var, 3)

print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:
```
Compare the manually calculated value and the observed practical value.
```
# Output
<img width="552" height="132" alt="image" src="https://github.com/user-attachments/assets/49772e1a-9e53-44c2-a7be-16f790dbd9c1" />

# Results:
```
Write the conclusion
```
