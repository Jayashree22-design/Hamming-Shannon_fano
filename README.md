# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
Google Colab

# Program:
```
#Huffman and Shannon-Fano coding
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:

<img width="1600" height="1148" alt="WhatsApp Image 2026-05-11 at 9 48 43 PM" src="https://github.com/user-attachments/assets/4f02cd2d-55fa-471a-89a1-15e026f0c4be" />
<img width="1113" height="1600" alt="WhatsApp Image 2026-05-11 at 9 35 43 PM (1)" src="https://github.com/user-attachments/assets/b75eb344-98e8-47e6-87e1-d7bb3431917c" />
<img width="1600" height="921" alt="WhatsApp Image 2026-05-11 at 9 52 10 PM (1)" src="https://github.com/user-attachments/assets/48d345f4-bcf3-4c07-8965-2445bf017190" />

<img width="1472" height="1600" alt="WhatsApp Image 2026-05-11 at 9 48 00 PM" src="https://github.com/user-attachments/assets/189b32d5-d167-40ce-94bb-e5d04d083782" />
<img width="994" height="1600" alt="WhatsApp Image 2026-05-11 at 9 52 10 PM" src="https://github.com/user-attachments/assets/8a03a5a7-bc10-4118-acf3-e9f1a80a07e8" />

# Output
```
Enter the number of Samples : 7
Enter the probability of sample values 1: 0.125
Enter the probability of sample values 2: 0.0625
Enter the probability of sample values 3: 0.25
Enter the probability of sample values 4: 0.0625
Enter the probability of sample values 5: 0.125
Enter the probability of sample values 6: 0.125
Enter the probability of sample values 7: 0.25
Enter the length of the sample values 1: 3
Enter the length of the sample values 2: 4
Enter the length of the sample values 3: 2
Enter the length of the sample values 4: 4
Enter the length of the sample values 5: 3
Enter the length of the sample values 6: 3
Enter the length of the sample values 7: 2
Average Codeword Length is : 2.625
Entropy is : 2.625
Efficiency is : 1.0
Redudancy is : 0.0
Variance is : 0.484
``` 
# Results:
```
The Huffman and Shannon-Fano of the given statistics {0.125,0.0625,0.25,0.0625,0.125,0.125,0.25} using python are verified.
```
