# 🟢 HTTP Basics - Developer

Secure Coding:
1. Always validate HTTP headers
2. Use framework HTTP parsing
3. Never parse requests manually
4. Implement request size limits

Secure Example (Python Flask):
from flask import Flask, request

@app.route('/api', methods=['POST'])
def api():
    data = request.get_json()
    if not validate(data):
        return {'error': 'Invalid'}, 400
    return process(data)

Best Practices:
- Use HTTPS everywhere
- Set security headers
- Rate limiting
- Input validation
