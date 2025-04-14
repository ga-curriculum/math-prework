## **Key Probability Concepts**

We're going to use Python to explore some Probability Concepts. 

We often interpret probability like a frequency. If I run an experiment over and over again and one outcome, call it A, occurs frequently, we might say the Probability of A is high. On the other end, if I run an experiment and outcome A happens infrequently, we might say that the Probability of A is low.

---

## Definitions, Notation, and Facts

Whenever you learn probability, there are some definitions that need to be established upfront to explain the concepts.

* Set: An unordered collection of distinct objects
    * {'A', 1, 2}

* Element: An object that is a member of a set
    * The above example of a set, 'A', 1, and 2 are all elements

*Note: Sets are actually a built-in datatype in Python and we'll use them to explain some concepts in a moment!*

### Some Notation

You'll typically see probability expressed in notation as:

    P(A)

Where P is the Probability, and A is an event. We interpret this as "The Probability of Event A occuring is..."

### Key Probability Facts
1. P(S) = 1: The probability that something happens is 1 (We'll talk about S in a moment).
2. P(ø) = 0: The probability that nothing happens is 0.
3. 0 ≤ P(A) ≤ 1: The probability of any given event is between 0 and 1.

---

## Concepts


### **1. Sample Space (S)**
The **sample space** is the set of all possible outcomes of a probability experiment.

#### **Example: Rolling a 6-sided die**
The sample space is:
```
S = {1, 2, 3, 4, 5, 6}
```


#### **Python Implementation**
```python
sample_space_dice = {1, 2, 3, 4, 5, 6}
print("Sample Space:", sample_space_dice)
```

---

### **2. Unions (A ∪ B)**
The **union** of two events **A** and **B** consists of all outcomes that are in **A**, **B**, or both.


definition:
```
P(A ∪ B) = P(A) + P(B) - P(A ∩ B)
```

#### **Example: Probability of rolling a number ≤ 3 or an even number**
- **A:** Rolling ≤ 3 → `A = {1, 2, 3}`
- **B:** Rolling an even number → `B = {2, 4, 6}`
- **A ∩ B:** Rolling a 2 → `A ∩ B = {2}`

#### **Base Python Implementation**
```python
A = {1, 2, 3}  # Rolling ≤ 3
B = {2, 4, 6}  # Rolling an even number

union_AB = A | B  # Union of A and B
intersection_AB = A & B  # Intersection of A and B

prob_A = len(A) / len(sample_space_dice)
prob_B = len(B) / len(sample_space_dice)
prob_intersection = len(intersection_AB) / len(sample_space_dice)

prob_union = prob_A + prob_B - prob_intersection

print("P(A or B) =", prob_union)
```

---

### **3. Intersections (A ∩ B)**
The **intersection** of two events consists of the outcomes that **both** A and B share.
```
P(A ∩ B) = P(A) × P(B)  (if A and B are independent)
```

---

### **4. Independence**
Two events **A** and **B** are **independent** if the occurrence of one does **not** affect the probability of the other.

```
P(A ∩ B) = P(A) × P(B)
```

#### **Example: Flipping a Coin and Rolling a Die**
- **A:** Getting heads on a coin flip → `P(A) = 0.5`
- **B:** Rolling a 3 on a die → `P(B) = 1/6`
- **Since these are independent events:**
```
P(A ∩ B) = P(A) × P(B) = 0.5 × (1/6) = 1/12
```

#### **Base Python Implementation**
```python
prob_heads = 0.5
prob_roll_3 = 1/6

prob_independent = prob_heads * prob_roll_3
print("P(A and B) for independent events:", prob_independent)
```

---

### **5. Conditional Probability (P(A | B))**
**Conditional probability** tells us the probability of event **A** happening **given that B has already happened**:
```
P(A | B) = P(A ∩ B) / P(B)
```

#### **Example: Drawing a Red Card Given it's a Face Card**
- **A:** Drawing a red card `(P(A) = 26/52)`
- **B:** Drawing a face card `(P(B) = 12/52)`
- **A ∩ B:** Drawing a red face card `(P(A ∩ B) = 6/52)`

```
P(A | B) = (P(A ∩ B) / P(B)) = (6/52) / (12/52) = 6/12 = 0.5
```

#### **Base Python Implementation**
```python
prob_A = 26/52  # Probability of drawing a red card
prob_B = 12/52  # Probability of drawing a face card
prob_A_and_B = 6/52  # Probability of drawing a red face card

prob_A_given_B = prob_A_and_B / prob_B  # Conditional probability formula
print("P(A | B):", prob_A_given_B)
```

---

### **Summary**
| Concept            | Definition & Formula                                      | Python Example |
|--------------------|----------------------------------------------------------|---------------|
| **Sample Space**  | Set of all possible outcomes                              | `{1, 2, 3, 4, 5, 6}` |
| **Union (A ∪ B)** | Outcomes in A or B or both. `P(A ∪ B) = P(A) + P(B) - P(A ∩ B)` | `A | B` |
| **Intersection (A ∩ B)** | Outcomes in both A and B. `P(A ∩ B)` | `A & B` |
| **Independence**  | `P(A ∩ B) = P(A) × P(B)` if independent.      | `prob_A * prob_B` |
| **Conditional Probability** | `P(A | B) = P(A ∩ B) / P(B)`        | `prob_A_and_B / prob_B` |

---


