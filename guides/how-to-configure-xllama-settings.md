---
description: This page explains the settings for configuring XLlama.
---

# How to configure XLlama settings

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

#### Ollama Configuration

* **API URL**\
  The default URL is `http://localhost:11434` and usually doesn't need to be changed.
* **Model Name**\
  The dropdown shows all Ollama models currently installed on your machine.\
  Learn how to install more models →

***

#### Global Settings

* **Default Prompt**\
  This prompt is used when you click the **Run XLlama** button in the Excel ribbon. It’s the main instruction you give to the model (e.g., "Summarize this data in one sentence").
* **Default System Prompt**\
  This defines the AI's behavior and tone. Unlike the default prompt, it doesn’t get replaced per run.\
  For example: _You are a helpful AI assistant who explains things clearly and concisely._
* **AI Output Sheet Name**\
  When you run XLlama, the add-in creates a new sheet in the workbook with this name and places the AI's response there.
