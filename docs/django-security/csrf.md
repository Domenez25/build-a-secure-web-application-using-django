# Cross-Site Request Forgery (CSRF) Protection

## Overview
CSRF involves tricking a user into submitting a malicious request unknowingly.

## Django’s Protection Mechanisms
- **CSRF Middleware**: Enabled by default to protect against CSRF attacks.
- **CSRF Tokens**: Automatically included in forms and validated.

## Example
```html
<!-- Form with CSRF token -->
<form method="post">
    {% csrf_token %}
    <!-- form fields -->
    <button type="submit">Submit</button>
</form>
```

## Best Practices
- Ensure CSRF protection middleware is enabled.
- Include {% csrf_token %} in all forms.
- Use CSRF tokens in AJAX requests.