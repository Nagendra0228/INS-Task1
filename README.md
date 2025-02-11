# INS-Task1
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1HO7elKLuxtCS476rGlrZfezYkirrg77e?usp=sharing)

1. Playfair Cipher
The Playfair cipher operates using a 5×5 key matrix and encrypts digraphs (pairs of letters) at a time.

Encryption Complexity
Preprocessing (Remove spaces, duplicate letters handling): O(n)
Matrix Lookup (Finding each letter in the 5×5 matrix): O(1) (constant time lookup)
Encryption Steps (Replacing letter pairs based on rules): O(n)
Each letter lookup is O(1) since it’s in a fixed-size 5×5 matrix.
Since pairs are processed together, the number of operations is O(n/2) = O(n).
✅ Total Complexity: O(n)

Decryption Complexity
Since decryption is simply the reverse of encryption with similar matrix lookups, it also takes O(n) time.
✅ Total Complexity: O(n)


2. Hill Cipher
The Hill cipher is a block cipher that encrypts plaintext using matrix multiplication.

Encryption Complexity
Convert text to numerical representation: O(n)
Reshape plaintext into a matrix: O(n)
Matrix Multiplication (Key Matrix × Plaintext Matrix): O(m³) (for an m × m key matrix)
Using Strassen’s algorithm, it can be reduced to O(m².81).
For 2×2 matrices, this becomes O(1) (constant).
For larger key matrices (e.g., 3×3, 4×4), the multiplication grows.
✅ Total Complexity: O(m³) + O(n) ≈ O(n) for small key sizes
✅ For large matrices, O(m².81) + O(n) ≈ O(m².81)

Decryption Complexity
Computing Modular Inverse of Key Matrix: O(m³)
Matrix Multiplication (Inverse Key × Cipher Matrix): O(m³)
Convert numbers back to text: O(n)
✅ Total Complexity: O(m³) + O(n) ≈ O(m³) (dominated by matrix inverse and multiplication)


2. Hill Cipher
The Hill cipher is a block cipher that encrypts plaintext using matrix multiplication.

Encryption Complexity
Convert text to numerical representation: O(n)
Reshape plaintext into a matrix: O(n)
Matrix Multiplication (Key Matrix × Plaintext Matrix): O(m³) (for an m × m key matrix)
Using Strassen’s algorithm, it can be reduced to O(m².81).
For 2×2 matrices, this becomes O(1) (constant).
For larger key matrices (e.g., 3×3, 4×4), the multiplication grows.
✅ Total Complexity: O(m³) + O(n) ≈ O(n) for small key sizes
✅ For large matrices, O(m².81) + O(n) ≈ O(m².81)

Decryption Complexity
Computing Modular Inverse of Key Matrix: O(m³)
Matrix Multiplication (Inverse Key × Cipher Matrix): O(m³)
Convert numbers back to text: O(n)
✅ Total Complexity: O(m³) + O(n) ≈ O(m³) (dominated by matrix inverse and multiplication)


3. Vigenère Cipher
The Vigenère cipher is a polyalphabetic substitution cipher where each letter is shifted based on a repeating key.

Encryption Complexity
Preprocessing (Key Expansion to match plaintext length): O(n)
Shift each letter based on the key: O(n)
Each character transformation is a simple modulo operation (O(1) per character).
✅ Total Complexity: O(n)

Decryption Complexity
Decryption is the inverse operation of encryption, with each letter being shifted backward.
It involves the same number of steps: O(n).
✅ Total Complexity: O(n)




