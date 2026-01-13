# HTTP Basics - Theory

## What is HTTP?

HyperText Transfer Protocol (HTTP) is the foundation of data communication on the web.

## HTTP Request Structure
GET /path HTTP/1.1
Host: example.com
User-Agent: Mozilla/5.0
Content-Type: application/json
Content-Length: 42
{"key": "value"}
## Components

1. **Request Line**: Method, Path, Version
2. **Headers**: Metadata about request
3. **Body**: Optional data payload

## Common HTTP Methods

- GET: Retrieve resource
- POST: Submit data
- PUT: Update resource
- DELETE: Remove resource
- OPTIONS: Check methods
- HEAD: Get headers only

## HTTP Versions

- HTTP/1.0: One request per connection
- HTTP/1.1: Keep-alive connections
- HTTP/2: Multiplexing, binary
- HTTP/3: QUIC protocol

## Common Vulnerabilities

1. **Request Smuggling**: Desync between frontend/backend
2. **Response Splitting**: Inject headers via CRLF
3. **Header Injection**: Poison headers
4. **Parameter Pollution**: Duplicate parameters

## Learning Objectives

After this module:
- Understand HTTP protocol structure
- Identify common HTTP vulnerabilities
- Learn attack and defense techniques
- Implement secure HTTP handling
