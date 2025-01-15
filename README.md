# Post-Quantum Encryption and Decryption REST API
This repository contains a simple REST API for post-quantum encryption and decryption using Flask. The API provides endpoints to encrypt and decrypt messages using placeholder functions. You can replace these functions with actual post-quantum cryptography implementations as needed.

## Introduction
Creating a REST API for post-quantum encryption and decryption involves several steps. 

For this example, I'll use **Flask**, a lightweight WSGI web application framework in Python, and a hypothetical post-quantum cryptography library. 
Since there isn't a widely adopted standard library for post-quantum cryptography in Python, I'll use a placeholder for encryption and decryption functions. 
You can replace these with actual implementations from libraries like ```pqcrypto``` or ```liboqs``` once you have them integrated.

## Prerequisites

- Python 3.8 or higher
- `pip` (Python package installer)

## Installation

### 1. **Clone the Repository**

   ```bash
   git clone https://github.com/nithinmohantk/post-quantum-api.git
   cd post-quantum-api
   ```

### 2. **Create a Virtual Environment (Optional but Recommended)**

```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

### 3. **Install Dependencies**


```bash
pip install -r requirements.txt
```

If requirements.txt does not exist, create it with the following content:
```
Flask==2.0.1
```
## Running the Server
### 1. Start the Flask Application
```
python app.py
```
By default, the server will run on http://127.0.0.1:5000/.

### 2. Access the API

You can test the API using tools like curl, Postman, or any HTTP client.

### 3. Using the API
#### 3.1 Encrypt a Message
**Endpoint: /encrypt**
**Method: POST**
- Request Body: JSON object with a message field (base64 encoded)

```json
{
  "message": "SGVsbG8gV29ybGQh"  // "Hello World!" in base64
}
```
- Response: JSON object with a ciphertext field (base64 encoded)
```json
{
  "ciphertext": "SGVsbG8gV29ybGQh"  // Placeholder response
}
```
#### 3.2 Decrypt a Message
**Endpoint: /decrypt**
**Method: POST**
- Request Body: JSON object with a ciphertext field (base64 encoded)
```json
{
  "ciphertext": "SGVsbG8gV29ybGQh"  // Placeholder response
}
```
- Response: JSON object with a message field (base64 encoded)
```json
{
  "message": "SGVsbG8gV29ybGQh"  // "Hello World!" in base64
}
```

### Notes
- **Security:** This example is for educational purposes and does not include security measures such as HTTPS, authentication, or input validation. Consider implementing these for a production environment.
- **Cryptography:** The pq_encrypt and pq_decrypt functions are placeholders. Replace them with actual post-quantum cryptography implementations as needed.
### License
This project is licensed under the MIT License - see the LICENSE file for details.