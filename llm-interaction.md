# Overview

This file contains commonly used code snippets for connecting or using Ollama or OpenAI with our codebase.

## Basic Conversation

### OpenAI

```py
openai = OpenAI(base_url = 'http://localhost:11434/v1', api_key = 'ollama')

message = "your message"

input_message = [
    {"role": "system", "content": "system message goes here"},
    {"role": "user", "content": "user message goes here"}
]

response = openai.chat.completions.create(model = "model_name", messages = input_message)

print(response.choices[0].message.content)
```

### Ollama Python Library

```py
OLLAMA_API = "http://localhost:11434/api/chat"
HEADERS = {"Content-Type":"application/json"}
MODEL = "llama3.2"

message = "your message"

payload = {
        "model": MODEL,
        "messages": [
            {"role": "system", "content": system_prompt},
            {"role": "user", "content": task_description}
        ],
        "stream": False
    }

response = requests.post(OLLAMA_API, json=payload, headers=HEADERS)

    if response.status_code == 200:
        try:
            json_response = response.json()

        except Exception as e:
            return f"Error parsing JSON: {e}"
    else:
        return f"Error: {response.status_code} - {response.text}"
```

## Types of Prompts

Models like GPT4o have been trained to receive instructions in a particular way. They expect to receive:

- **A System Prompt** that tells them what task they are performing and what tone they should use
- **A User Prompt** that conversation starter that they should reply to.
