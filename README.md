# Determine if Two Strings Are Close

## Problem Description

Two strings are considered **close** if you can transform one into the other using the following operations any number of times:

1. **Swap any two existing characters.**  
   Example: `"abcde"` → `"aecdb"`

2. **Transform every occurrence of one existing character into another existing character**, and **do the same with the other character** (i.e., swap all instances of two characters).  
   Example: `"aacabb"` → `"bbcbaa"` (all `a` → `b` and all `b` → `a`)

**Given two strings** `word1` and `word2`, **return `true` if they are close**, otherwise return `false`.

---

## Examples

### Example 1:
**Input:**  
`word1 = "abc"`  
`word2 = "bca"`  
**Output:**  
`true`

**Explanation:**  
You can transform `"abc"` → `"bca"` using two swaps. ✅

---

### Example 2:
**Input:**  
`word1 = "a"`  
`word2 = "aa"`  
**Output:**  
`false`

**Explanation:**  
The characters in `word2` include more of `'a'` than in `word1`. No operation can insert new characters. ❌

---

### Example 3:
**Input:**  
`word1 = "cabbba"`  
`word2 = "abbccc"`  
**Output:**  
`true`

**Explanation:**  
- Apply Swap: `"cabbba"` → `"caabbb"`  
- Apply Transform: `a` ↔ `b` → `"baaccc"`  
- Apply Swap: `"baaccc"` → `"abbccc"` ✅

---

## Constraints

- `1 <= word1.length, word2.length <= 10⁵`
- `word1` and `word2` contain only lowercase English letters (`'a'` to `'z'`)
