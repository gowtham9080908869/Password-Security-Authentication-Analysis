# Password-Security-Authentication-Analysis

1. How Passwords Are Stored (Hashing vs Encryption)
- Hashing:
- One-way mathematical function.
- Converts a password into a fixed-length string (digest).
- Cannot be reversed to reveal the original password.
- Example: password123 → 482c811da5d5b4bc6d497ffa98491e38 (MD5).
- Used for password storage in databases.
- Encryption:
- Two-way process (encrypt & decrypt).
- Requires a key to decrypt back to the original password.
- Example: AES encryption can restore the original password if the key is known.
- Best Practice: Passwords should never be stored in plain text. Hashing with a salt (random data added before hashing) is the standard.
- 
2. Cracking Weak Hashes Using Wordlists
- Wordlist Attack:
- Uses precompiled lists of common passwords (e.g., rockyou.txt).
- Hashes each word and compares with stored hash.
- Tools: hashcat, John the Ripper.
- Example: MD5 hash 482c811da5d5b4bc6d497ffa98491e38 → cracked as password123.

3. Brute Force vs Dictionary Attacks
- Brute Force Attack
- Tries all possible combinations.
- Guaranteed success but extremely slow for long/complex passwords.
- Dictionary Attack
- Uses known password lists.
- Faster but limited to weak/common passwords.
- Hybrid Attack
- Combines dictionary words with variations (e.g., Password1!).

4. Why Weak Passwords Fail
- Short length (e.g., 12345).
- Predictable patterns (qwerty, abc123).
- Password reuse across multiple accounts.
- Lack of complexity (no uppercase, numbers, or symbols).
- Attackers exploit human tendencies for simplicity.

5. Multi‑Factor Authentication (MFA) & Importance
- MFA Factors:
- Something you know (password).
- Something you have (phone, token).
- Something you are (fingerprint, face).
- Benefits:
- Even if a password is stolen, attackers cannot access the account without the second factor.
- Protects against phishing, credential stuffing, brute force.

6. Recommendations for Strong Authentication
✅ Use bcrypt, scrypt, or Argon2 for password hashing.
✅ Enforce minimum length (12+ characters) and complexity rules.
✅ Implement account lockouts after repeated failed attempts.
✅ Require MFA for sensitive accounts.
✅ Encourage password managers to generate unique, random passwords.
✅ Regularly audit and update authentication policies.
✅ Educate users about phishing and social engineering risks.






