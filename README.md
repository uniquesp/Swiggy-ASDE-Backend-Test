# Swiggy-ASDE-Backend-Test  (03-07-24)

## ALL Solutions are Provided in above files

---

## DSA Question: Extraordinary String

### Description

Each character of the English alphabet has been mapped to a digit as shown below.

![Alphabet to Digit Mapping](https://fastly.jsdelivr.net/gh/doocs/leetcode@main/solution/2900-2999/2950.Number%20of%20Divisible%20Substrings/images/old_phone_digits.png)

A string is **divisible** if the sum of the mapped values of its characters is divisible by its length.

Given a string `s`, return the number of **divisible substrings** of `s`.

A **substring** is a contiguous non-empty sequence of characters within a string.

#### Example 1:

| Substring | Mapped | Sum | Length | Divisible? |
|-----------|--------|-----|--------|------------|
| a         | 1      | 1   | 1      | Yes        |
| s         | 7      | 7   | 1      | Yes        |
| d         | 2      | 2   | 1      | Yes        |
| f         | 3      | 3   | 1      | Yes        |
| as        | 1, 7   | 8   | 2      | Yes        |
| sd        | 7, 2   | 9   | 2      | No         |
| df        | 2, 3   | 5   | 2      | No         |
| asd       | 1, 7, 2| 10  | 3      | No         |
| sdf       | 7, 2, 3| 12  | 3      | Yes        |
| asdf      | 1, 7, 2, 3| 13| 4     | No         |

**Input:** `word = "asdf"`  
**Output:** `6`  
**Explanation:** The table above contains the details about every substring of the word, and we can see that 6 of them are divisible.

#### Example 2:

**Input:** `word = "bdh"`  
**Output:** `4`  
**Explanation:** The 4 divisible substrings are: "b", "d", "h", "bdh".  
It can be shown that there are no other substrings of the word that are divisible.

#### Example 3:

**Input:** `word = "abcd"`  
**Output:** `6`  
**Explanation:** The 6 divisible substrings are: "a", "b", "c", "d", "ab", "cd".  
It can be shown that there are no other substrings of the word that are divisible.

#### Constraints:
- `1 <= word.length <= 2000`
- `word` consists only of lowercase English letters.

---

## SQL Question: Binary Tree

### Description

You are given a table, BST, containing two columns: `N` and `P`, where `N` represents the value of a node in a Binary Tree, and `P` is the parent of `N`.

Write a query to find the node type of each Binary Tree node ordered by the value of the node. The possible node types are:
- **Root**: If the node is the root of the tree.
- **Leaf**: If the node is a leaf node.
- **Inner**: If the node is neither root nor a leaf node.

### Sample Input

```
 BST Table
 N  |  P
----|----
 1  |  2
 3  |  5
 6  |  8
 8  |  6
 9  |  3
```

### Sample Output

```
1 Leaf
2 Inner
3 Leaf
5 Root
6 Leaf
8 Inner
9 Leaf
```

### Explanation

The Binary Tree below illustrates the sample input:

![Binary Tree](https://s3.amazonaws.com/hr-assets/0/1532493154-b45f2a6d3a-Binary_Tree.png)

- **Root**: Node with value 5.
- **Inner**: Nodes with values 2 and 8.
- **Leaf**: Nodes with values 1, 3, 6, and 9.

Refer to the [problem statement](https://www.hackerrank.com/challenges/binary-search-tree-1/problem) for more details and constraints.

---

## REST API Question: Discounted Price

### Description

REST API: Discounted Price

Given a barcode, query the API at `https://jsonmock.hackerrank.com/api/inventory?barcode={barcode}` and return the item's discounted price.

The response is a JSON object with 5 fields. The essential field is `data`.

In the `data` array, the item has the following schema:

- **barcode**: the barcode for the product (String)
- **price**: the gross selling price (Number)
- **discount**: the discount percent to apply (Number)

Fields such as `page`, `per_page`, `total`, `total_pages`, etc., are not required for this task.

If the barcode is found, the `data` array contains exactly 1 element. If not, it is empty, and the function should return -1.

An example of the product record from `https://jsonmock.hackerrank.com/api/inventory?barcode=74001755` is:

```json
{
    "barcode": "74001755",
    "item": "Ball Gown",
    "category": "Full Body Outfits",
    "price": 785,
    "discount": 7,
    "available": 1
}
```

## ALL THE BEST

