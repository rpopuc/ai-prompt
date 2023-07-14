# AI Prompt

Implementation of a (toy) command called `ai-prompt` that use prompt template files to prompt OpenAIs API.

## How it works

The command gets the prompt templates in the `~/prompt-templates` directory. Then, it lists the files and asks the user to choose which one to use. So,the command parses the template file, gets the replacement words (in the format {word}) and asks the user for the replacement values. Then, it uses the OpenAI API to get the response to the prompt.

## Setup

Install dependencies:

```
pip3 install -r requirements.txt
```

This script uses the OpenAI API. Therefore, you should create an OpenAI API account, obtain an API key, and set that key as an environment variable before executing it. To get your API key, access https://platform.openai.com/account/api-keys and set it in the environment using:

```
export OPENAI_API_KEY=<your-api-key>
```

## Use

Execute with python:

```
python3 ai-prompt.py
```
