# Prompt Injection Defense for Trustworthy LLMs
## Overview

This project builds a simple and effective defense system against prompt injection attacks on Large Language Models (LLMs).
It checks every user prompt for unsafe or manipulative patterns before sending it to the model.
If a prompt is flagged as unsafe, it is blocked and never reaches the model.
If the prompt is safe, it is processed normally and the model generates a response.

## Why This Project

LLMs can be tricked by malicious prompts like
“ignore previous instructions” or “reveal your system prompt.”
Such inputs can lead to information leaks or rule violations.
This project improves the privacy and security of LLMs by adding a protection layer that filters harmful text before it is processed.

## Features

Detects prompt injection using regular expressions and keyword scanning

Blocks unsafe inputs with clear logging

Processes safe prompts using an open-source LLM

Includes accuracy testing for the detection system

Runs locally or in Google Colab using GPU for better performance

## Model Used

The project uses Mistral-7B-v0.1 from Hugging Face.
This model is open source, efficient, and performs well for general text generation tasks.
It was chosen because it does not require gated access and supports GPU acceleration in Colab.

## How It Works

User input is scanned for suspicious keywords or patterns.

If an attack is detected, the input is blocked.

Safe inputs are tokenized and sent to the model.

The model generates a secure response.

The system logs the result with a timestamp for transparency.

## Setup

Open the notebook in Google Colab.

Install required libraries:

!pip install transformers accelerate torch -q


Run each cell in order.

Use your own Hugging Face token if needed for model download.

## Evaluation

The project includes an evaluation script that checks accuracy by comparing expected and detected results on sample prompts.
This helps measure how well the defense system performs in identifying harmful inputs.


## Applications

Safe chatbot development

Secure LLM research

Educational use for AI ethics and security

Integration into enterprise AI systems for risk mitigation

## Conclusion

This project demonstrates a simple yet powerful method to make large language models more trustworthy.
It shows how rule-based defenses can protect AI systems from manipulative user inputs, ensuring responsible and secure model use.
