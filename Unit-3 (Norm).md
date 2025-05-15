# Functional Dependencies and Inference Rules

## What are Functional Dependencies?

A **functional dependency (FD)** is a relationship between two sets of attributes in a database relation. It describes how one set of attributes uniquely determines another set. In other words, if you know the value of one attribute (or a group of attributes), you can determine the value of another attribute (or group of attributes).

**Definition:**

- For a relation R, a functional dependency X → Y means that if two tuples (rows) have the same value for attributes X, they must also have the same value for attributes Y.
- X is called the **determinant**, and Y is the **dependent**.

**Example:**

- If StudentID → Name, then knowing the StudentID, you can uniquely determine the Name.

---

![Armstrong's Axioms](https://media.geeksforgeeks.org/wp-content/uploads/20250422123933036205/axioms.webp)

## Basic Inference Rules (Armstrong's Axioms)

To reason about functional dependencies, we use a set of rules called **Armstrong's Axioms**. These rules help us infer all possible FDs from a given set.

### 1. **Reflexivity Rule**

If Y is a subset of X, then X → Y.

### 2. **Augmentation Rule**

If X → Y, then XZ → YZ (for any set of attributes Z).

### 3. **Transitivity Rule**

If X → Y and Y → Z, then X → Z.

**Additional Derived Rules:**

- **Union:** If X → Y and X → Z, then X → YZ.
- **Decomposition:** If X → YZ, then X → Y and X → Z.
- **Pseudo-Transitivity:** If X → Y and YZ → W, then XZ → W.

---

## Example Proof: AD → F

Given:

- R(A, B, C, D, E, F)
- FDs: A → BC, B → E, CD → EF

**To Prove:** AD → F

### Step-by-Step Solution

1. **List the FDs:**

   - A → BC
   - B → E
   - CD → EF

2. **Find the closure of AD (AD⁺):**

   - Start with AD = {A, D}

3. **Apply FDs to AD:**

   - A → BC: Since A is in AD, add B and C. Now we have {A, D, B, C}
   - B → E: B is now in the set, so add E. Now we have {A, D, B, C, E}
   - CD → EF: C and D are in the set, so add E and F. Now we have {A, D, B, C, E, F}

4. **Check if F is in AD⁺:**
   - Yes, F is in the closure.

**Conclusion:**

- Since F is in the closure of AD, **AD → F** holds.

---

## Summary Table

| Given FDs | Closure Steps for AD | Resulting Attributes |
| --------- | -------------------- | -------------------- |
| A → BC    | AD + BC              | A, D, B, C           |
| B → E     | + E                  | A, D, B, C, E        |
| CD → EF   | + F (and E again)    | A, D, B, C, E, F     |

**Therefore, AD → F is a valid functional dependency in R.**

---
