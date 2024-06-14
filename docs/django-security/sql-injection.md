# SQL Injection Protection

## Overview
SQL Injection is a code injection technique that exploits vulnerabilities in an application’s software by manipulating SQL queries.

## Django’s Protection Mechanisms
- **ORM (Object-Relational Mapping)**: Django’s ORM automatically escapes parameters used in queries, preventing SQL injection.
- **Parameterized Queries**: Always use parameterized queries to avoid injecting raw SQL.

## Example
```python
# Vulnerable code
user = User.objects.raw("SELECT * FROM auth_user WHERE username = '%s'" % username)

# Safe code using ORM
user = User.objects.get(username=username)
```

## Best Practices
- Avoid using raw() for SQL queries.
- Use Django’s ORM to interact with the database securely.