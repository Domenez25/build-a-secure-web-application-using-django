# Content Security Policy (CSP)

## Overview
CSP helps prevent XSS, clickjacking, and other code injection attacks by specifying valid sources for content.

## Django’s Protection Mechanisms
- **Middleware**: Use middleware to set CSP headers.

## Example
```python
# middleware.py
from django.utils.deprecation import MiddlewareMixin

class ContentSecurityPolicyMiddleware(MiddlewareMixin):
    def process_response(self, request, response):
        response['Content-Security-Policy'] = "default-src 'self';"
        return response
```
## Best Practices
- Define a strict CSP for your application.
- Regularly review and update your CSP policies.
- Use report-only mode to test policies before enforcement.