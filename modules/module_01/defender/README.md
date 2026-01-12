# 🔵 HTTP Basics - Defender

Detection Methods:
1. Monitor chunked encoding anomalies
2. Detect multiple Content-Length headers
3. Log suspicious Host headers

Mitigation:
- Use HTTP/2 exclusively
- Deploy WAF rules
- Strict request validation

WAF Rule Example:
if Transfer-Encoding AND Content-Length present
then BLOCK request
