## Question Answering API with Chroma

This project provides a simple API for answering questions using similarity search directly, or by using similarity search to provide documents as context to an LLM.

## Installation To install the required dependencies, run:

`pip install -r requirements.txt`

## Usage 
To use the API, you need to start the server by running the QuestionAnswering.py file:

`python QuestionAnswering.py`

This will start the server on http://localhost:5000. You can then send a POST request to the /answer endpoint with a JSON payload containing the question:

```
import requests

url = 'http://localhost:5000/answer' data = {'question': 'What is the capital of France?'} response = requests.post(url, json=data)

print(response.json())
```

This code will send a POST request to the /answer endpoint with a JSON payload containing the question "What is the capital of France?". It will then print the response from the server.

Alternatively, you can use curl

```
curl -X POST -H "Content-Type: application/json" -d '{"question": "What is the capital of France?"}' http://localhost:5000/answer
```

## Configuration
The config.json file contains the configuration for the API, including the API key for the LLM