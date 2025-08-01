# KS-KEY-Authentication-System-with-OTP-Verification


 # KS-KEY Authentication System with OTP Verification

This Python project implements a simple yet secure user authentication system using a custom key generation algorithm (`KS-KEY`) and a One-Time Password (OTP) verification step.

##Features

- **Custom Key-Based Password Hashing:**  
  Uses a unique binary transformation (`KS-KEY algorithm`) to generate a secure key from user-provided passwords.

- **SHA-256 Hashing:**  
  Transforms the generated key into a secure hash using SHA-256.

- **OTP-Based Two-Factor Authentication (2FA):**  
  A randomly generated 6-digit OTP is required after the password step to simulate 2FA.

- **In-Memory User Database:**  
  All user credentials are stored in a dictionary for demonstration purposes.

## Technologies Used

- Python 3
- `hashlib` for secure hashing
- `random` for OTP generation
- `input()` for user interaction

## How It Works

1. **Registration:**
   - User provides a username and password.
   - The password is converted into a binary key using the custom `ks_key_algorithm`.
   - The key is hashed using SHA-256 and stored in an in-memory dictionary.

2. **Authentication:**
   - User provides the username and password.
   - The password is reprocessed and hashed.
   - If the hash matches the stored hash, an OTP is sent (printed in this demo).
   - User must enter the correct OTP to complete the login.

## Example

```bash
== REGISTER USER ==
Enter username: john
Create password: secret123
User 'john' registered with hashed key.

== USER LOGIN ==
Enter username: john
Enter password: secret123
[DEBUG] OTP sent via email: 654321
Enter the OTP: 654321
[✔] Login successful.

