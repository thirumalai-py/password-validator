# Password Strength Validator

## Description
This Python function validates and checks the strength of a password based on various security criteria. It ensures that passwords meet minimum security standards and categorizes their strength as **Weak, Medium, or Strong**.

## Features
- Validates password length (minimum 8 characters required)
- Ensures at least:
  - 1 uppercase letter (A-Z)
  - 1 lowercase letter (a-z)
  - 1 digit (0-9)
  - 1 special character (!, @, #, $, etc.)
- Prevents spaces within the password
- Assesses password strength based on:
  - Length (longer passwords score higher)
  - Number of special characters (more than 2 increases strength)
  - Combination of letters, numbers, and symbols
- Returns a detailed response including error messages and strength level

## Usage
### Function Definition
```python
def check_password_strength(password: str):
```
### Returns:
- **If the password is invalid:**
  - `error_count`: Number of validation errors
  - `errors`: List of reasons why the password is invalid
  - `strength`: "Weak"
- **If the password is valid:**
  - `error_count`: 0
  - `message`: "Password is valid"
  - `strength`: "Weak", "Medium", or "Strong"

### Example Usage
```python
password = "P@ssw0rd123!"
result = check_password_strength(password)
print(result)
```
### Example Outputs:
#### Weak Password:
```json
{
    "error_count": 3,
    "errors": [
        "Password should contain at least 1 uppercase letter",
        "Password should contain at least 1 digit",
        "Password should contain at least 1 special character"
    ],
    "strength": "Weak"
}
```
#### Strong Password:
```json
{
    "error_count": 0,
    "message": "Password is valid",
    "strength": "Strong"
}
```

## Installation & Requirements
- Python 3.x
- No external dependencies (uses built-in string functions)

## Best Practices for Strong Passwords
- Use at least **12+ characters**
- Include **uppercase, lowercase, numbers, and symbols**
- Avoid common words and patterns (e.g., "password123")
- Do not reuse passwords across accounts

## License
This script is open-source and free to use for any purpose.

## Contributions
Feel free to submit pull requests or suggest improvements!

