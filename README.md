# AI Prompt

Implementation of a (toy) command called `ai-prompt` that use prompt template files to prompt OpenAIs API.

## How it works

The prompt templates are obtained from the ~/prompt-templates directory by executing the command. Subsequently, the files are displayed in a list, and the user is prompted to select one. The command then proceeds to analyze the chosen template file, extracting the replacement words enclosed in {word} format, and requests the user to input the corresponding replacement values. Finally, the OpenAI API is utilized to generate a response based on the given prompt.

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

## Prompt template example

```
Act like a senior developer, giving instructions for a junior developer to solve what is asked. List all the files with path. Do not describe folders, only files. In order for the junior to be able to develop what was requested, the descriptions of the files must be as complete as possible, detailing the structure when necessary, for example, a class or a route file.
The response must have the following structure:

FILE: <file name>
DESCRIPTION: <Detailed description>

When, and only if, solution contains OOP entities, describe the all them with PlantUML, in the end of the response.

Ask: "{UserHistory}"
```