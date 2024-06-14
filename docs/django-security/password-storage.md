# Secure Password Storage

## Overview
Secure storage of passwords is crucial to protect user data.

## Django’s Protection Mechanisms
- **Password Hashing**: Django uses PBKDF2 by default for hashing passwords.
- **Password Validators**: Enforce strong password policies.

## Example
```python
from django.contrib.auth.models import User

# Creating a user with a hashed password
user = User.objects.create_user('username', 'email@example.com', 'password')
```

## Best Practices
- Use Django’s authentication system.
- Enforce strong password policies.
- Regularly update hashing algorithms.