# Cross-Site Scripting (XSS) Protection

## Overview
XSS allows attackers to inject malicious scripts into webpages viewed by other users.

## Django’s Protection Mechanisms
- **Auto-escaping**: Django templates escape variables by default.
- **Safe Markup**: Use `mark_safe()` only when you are sure the content is safe.

## Example
```html
<!-- Safe template usage -->
<p>{{ user_input }}</p>

<!-- Use mark_safe with caution -->
from django.utils.safestring import mark_safe
safe_input = mark_safe(user_input)
```
## Best Practices
- Validate and sanitize user inputs.
- Avoid using mark_safe() unless necessary.
- Keep third-party libraries updated.