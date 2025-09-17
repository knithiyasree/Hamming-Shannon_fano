# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
google colab
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


# Output
![WhatsApp Image 2025-09-17 at 13 21 22_5af0484a](https://github.com/user-attachments/assets/12c2aaa7-1f37-41e7-9a8b-efbc22b2caff)
![WhatsApp Image 2025-09-17 at 13 21 23_efaf0ea0](https://github.com/user-attachments/assets/0961be26-3cd2-4ef0-8aa1-819236598886)
![WhatsApp Image 2025-09-17 at 13 21 23_1d9d4c36](https://github.com/user-attachments/assets/e655d112-fc64-4923-bfa5-49827f099f24)

# Results:
The Huffman and Shannon-Fano coding techniques have been successfully applied to the given source. The average codeword length, entropy, variance, redundancy, and efficiency have been computed.



