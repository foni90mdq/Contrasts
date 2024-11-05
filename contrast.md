# Orthogonal Contrast Analysis: Example and Table Construction

In this example, we'll walk through the process of constructing an orthogonal contrast table for a control group (C) and four treatment groups (A, B, D, and E). Orthogonal contrasts are sets of comparisons that are statistically independent, meaning they don’t overlap in the information they test.

## Step 1: Set Up Your Groups and Define Comparisons
Suppose we have five groups:

- **C (Control)**
- **A, B, D, E (Treatment groups)**

Let's say we’re interested in testing the following contrasts:
1. **Contrast 1**: Compare the control group to all treatment groups combined.
2. **Contrast 2**: Compare group A with the average of groups B, D, and E.
3. **Contrast 3**: Compare the average of groups B and D with group E.

## Step 2: Assign Weights to Each Contrast
Each contrast is defined by weights assigned to the groups, representing the comparisons we want to make. The weights for each contrast must sum to zero and be orthogonal to each other (i.e., independent comparisons).

For our three contrasts:

1. **Contrast 1**: Compare the control (C) to all treatment groups (A, B, D, and E).
   - Weights: C = -4, A = +1, B = +1, D = +1, E = +1

2. **Contrast 2**: Compare treatment group A to the average of groups B, D, and E.
   - Weights: C = 0, A = +3, B = -1, D = -1, E = -1

3. **Contrast 3**: Compare the average of groups B and D with group E.
   - Weights: C = 0, A = 0, B = +1, D = +1, E = -2

## Step 3: Verify Orthogonality
To confirm orthogonality, the sum of the products of the weights for each pair of contrasts should equal zero. Here’s the check for each pair:

- **Contrast 1 x Contrast 2**:  
  (-4 \* 0) + (1 \* 3) + (1 \* -1) + (1 \* -1) + (1 \* -1) = 0

- **Contrast 1 x Contrast 3**:  
  (-4 \* 0) + (1 \* 0) + (1 \* 1) + (1 \* 1) + (1 \* -2) = 0

- **Contrast 2 x Contrast 3**:  
  (0 \* 0) + (3 \* 0) + (-1 \* 1) + (-1 \* 1) + (-1 \* -2) = 0

Each product sums to zero, confirming the contrasts are orthogonal.

## Step 4: Construct the Orthogonal Contrast Table
Now, we can lay out the weights in a table format:

| Group   | Contrast 1 | Contrast 2 | Contrast 3 |
|---------|------------|------------|------------|
| **C**   | -4         | 0          | 0          |
| **A**   | +1         | +3         | 0          |
| **B**   | +1         | -1         | +1         |
| **D**   | +1         | -1         | +1         |
| **E**   | +1         | -1         | -2         |

## Step 5: Interpret Each Contrast
Each row in the table represents one group, and each column under the contrasts represents the comparison weights for that contrast. After calculating the group means and applying these weights, you can run a t-test or ANOVA for each contrast to check for significance.
