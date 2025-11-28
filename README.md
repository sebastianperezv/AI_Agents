# 🤖 AI Agents: From Structured Output to LangGraph

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o-green)
![LangGraph](https://img.shields.io/badge/Orchestration-LangGraph-orange)

## 📖 Overview

This repository documents the progressive implementation of **AI Agents**, exploring different cognitive architectures ranging from simple deterministic validation to complex stateful graphs using **LangGraph**.

The goal of this project is to demonstrate how to control Large Language Models (LLMs) to perform specific tasks reliably, handle external data (RAG), and manage conversation states.

---

## 🚀 Projects & Architectures

This repository is organized into three main levels of complexity:

### 1. Structured Output Agent (JSON Mode)
* **File:** `Joke_bot.ipynb`
* **Core Concept:** **Determinism & Data Extraction**.
* **Description:** A simple agent that generates jokes but includes a strict validation layer. It forces the LLM to output valid **JSON** instead of free text. This allows the Python code to programmatically parse the response and decide if the topic is valid before showing it to the user.
* **Key Tech:** OpenAI API (`response_format={'type': 'json_object'}`).

### 2. The AI Sommelier (RAG & Tool Use)
* **File:** `AI_sommelier.py`
* **Core Concept:** **Retrieval Augmented Generation (RAG) & Semantic Routing**.
* **Description:** An autonomous agent acting as a Sommelier. It uses a **Vector Store** to retrieve information from a specific PDF document (`Vinhos_baba_d_urso.pdf`).
    * **Semantic Routing:** It detects if the user is talking about wine.
    * **Function Calling:** If the topic drifts (e.g., sports, politics), it triggers a specific tool (`escalate_to_boss`) to handle the handoff and end the session strictly.
* **Key Tech:** OpenAI Assistants SDK, Vector Stores, Function Calling (`@function_tool`).

### 3. Stateful Graph Agent (LangGraph)
* **File:** `Job_interview.ipynb`
* **Core Concept:** **State Management & Cyclic Flows**.
* **Description:** An advanced implementation using **LangGraph**. Unlike linear scripts, this agent maintains a persistent `AgentState` (TypedDict) that travels through nodes.
    * **Routers:** Logic functions that decide the next step (Conditional Edges).
    * **Loops:** If the validation fails, the graph routes back to itself, creating a self-correction loop until the input is valid or a recursion limit is reached.
* **Key Tech:** LangGraph, LangChain, StateGraph, TypedDict.

---

## 🛠️ Tech Stack

* **Language:** Python
* **LLM Provider:** OpenAI (GPT-4o)
* **Orchestration:** LangChain & LangGraph
* **Environment:** Google Colab / Jupyter Notebooks
