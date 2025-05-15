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
- **Composition Rule** If X → Y and B → Z, then XB → YZ.

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

## Normal Forms in Database Design

Normalization is the process of organizing data in a database to reduce redundancy and improve data integrity. It involves dividing large tables into smaller ones and defining relationships between them. Normal forms are a series of guidelines to achieve this.

### 1. **First Normal Form (1NF)**

A relation is in **1NF** if:

- All attributes contain only atomic (indivisible) values.
- Each column contains values of a single type.
- Each row is unique, identified by a primary key.

**Example:**

| StudentID | Name  | Subjects         |
| --------- | ----- | ---------------- |
| 1         | Alice | Math, Science    |
| 2         | Bob   | English, History |

**Problem:** The `Subjects` column contains multiple values, violating 1NF.

**Solution (1NF):**

| StudentID | Name  | Subject |
| --------- | ----- | ------- |
| 1         | Alice | Math    |
| 1         | Alice | Science |
| 2         | Bob   | English |
| 2         | Bob   | History |

---

### 2. **Second Normal Form (2NF)**

A relation is in **2NF** if:

- It is in 1NF.
- All non-prime attributes are fully functionally dependent on the primary key (no partial dependency).

**Example:**

| OrderID | ProductID | ProductName | Quantity |
| ------- | --------- | ----------- | -------- |
| 1       | 101       | Pen         | 10       |
| 1       | 102       | Notebook    | 5        |

**Problem:** `ProductName` depends only on `ProductID`, not the full composite key (`OrderID, ProductID`).

**Solution (2NF):**

**Orders Table:**

| OrderID | ProductID | Quantity |
| ------- | --------- | -------- |
| 1       | 101       | 10       |
| 1       | 102       | 5        |

**Products Table:**

| ProductID | ProductName |
| --------- | ----------- |
| 101       | Pen         |
| 102       | Notebook    |

---

### 3. **Third Normal Form (3NF)**

A relation is in **3NF** if:

- It is in 2NF.
- There are no transitive dependencies (non-prime attributes depend only on the primary key).

**Example:**

| EmployeeID | DepartmentID | DepartmentName |
| ---------- | ------------ | -------------- |
| 1          | 10           | HR             |
| 2          | 20           | IT             |

**Problem:** `DepartmentName` depends on `DepartmentID`, not directly on `EmployeeID`.

**Solution (3NF):**

**Employees Table:**

| EmployeeID | DepartmentID |
| ---------- | ------------ |
| 1          | 10           |
| 2          | 20           |

**Departments Table:**

| DepartmentID | DepartmentName |
| ------------ | -------------- |
| 10           | HR             |
| 20           | IT             |

---

### 4. **Boyce-Codd Normal Form (BCNF)**

A relation is in **BCNF** if:

- It is in 3NF.
- Every determinant is a candidate key.

**Example:**

| StudentID | CourseID | Instructor |
| --------- | -------- | ---------- |
| 1         | C101     | Prof. A    |
| 2         | C102     | Prof. B    |

**Problem:** `Instructor` depends on `CourseID`, not `StudentID`.

**Solution (BCNF):**

**Enrollments Table:**

| StudentID | CourseID |
| --------- | -------- |
| 1         | C101     |
| 2         | C102     |

**Courses Table:**

| CourseID | Instructor |
| -------- | ---------- |
| C101     | Prof. A    |
| C102     | Prof. B    |

---

### Summary of Normal Forms

| Normal Form | Key Requirement                                                                 |
| ----------- | ------------------------------------------------------------------------------- |
| 1NF         | Atomic values in attributes, unique rows.                                       |
| 2NF         | No partial dependency (non-prime attributes depend on the whole primary key).   |
| 3NF         | No transitive dependency (non-prime attributes depend only on the primary key). |
| BCNF        | Every determinant is a candidate key.                                           |

By applying these normal forms, databases become more efficient, consistent, and easier to maintain.
