# Overview

In this markdown, I have noted down:

- The commands I frequently used
- The libraries I used for development
- Project Structure

## Frequently Used Commands

### Ollama

Install Ollama [[Link](https://ollama.com/)]

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

To run a model. Here is the [complete list](https://ollama.com/search) of available models:

```bash
ollama run {model_name}
```

While running a LLM on Ollama, use `\?` to get all available command. And to exit, use `\bye` to exit the system.