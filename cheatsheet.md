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

### Setting up Environment

#### Conda

To install anaconda in ubuntu

```bash
curl -O https://repo.anaconda.com/archive/Anaconda3-2024.10-1-Linux-x86_64.sh

# after downloading
bash ~/Anaconda3-2024.10-1-Linux-x86_64.sh
```

Here are some basic conda commands:

- Verify conda installed, check version number: `conda info`
- Update conda to the current version: `conda update conda`
- Install a package included in Anaconda: `conda update PACKAGENAME`

| Task                                                                  | Command                                                    |
| --------------------------------------------------------------------- | ---------------------------------------------------------- |
| Create a new environment named py35, install Python 3.5               | `conda create --name py35 python=3.5`                      |
| Activate the new environment to use it                                | `WINDOWS: activate py35LINUX, macOS: source activate py35` |
| Get a list of all my environments, active environment is shown with * | `conda env list`                                           |
| Make exact copy of an environment | `conda create --clone py35 --name py35-2` |
| Save environment to a text file | `conda list --explicit > bio-env.txt`|
| Create environment from a text file | `conda env create --file bio-env.txt` |