📌 Overview

This project demonstrates how to interact with the Algorithmia API by making a POST request with input data and retrieving a response from a hosted algorithm. The provided code snippet shows both a curl request example and a Python client example.

🚀 Features

Makes API calls to Algorithmia

Sends input data ("Saturnre") to a demo algorithm

Demonstrates authentication with an API key

Provides both cURL and Python usage examples

📂 File Contents

statistics → Contains example API calls (cURL and Python).

⚙️ Requirements

To run the Python example, ensure you have:

Python 3.7+

algorithmia library

Install the library with:

pip install algorithmia

▶️ Usage
Using cURL
curl -X POST -d '"Saturnre"' \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Simple YOUR_API_KEY' \
  https://api.algorithmia.com/v1/algo/demo/Hello/

Using Python
import Algorithmia

# Replace with your API key
client = Algorithmia.client("YOUR_API_KEY")

# Call the demo algorithm
input = "Saturnre"
algo = client.algo("demo/Hello/0.1.1")
print(algo.pipe(input).result)

🔑 API Key

Replace YOUR_API_KEY with your personal Algorithmia API key.

Keep your key secure and never commit it to version control.

📖 References

Algorithmia API Docs
