# Math ReAct Agent

This repository contains a **functional AI agent built from scratch**, without using LangChain or other agent frameworks.  
The project focuses on implementing a **ReAct-style (Reason + Act) agent loop** using plain Python, explicit control logic, and a lightweight UI.

The emphasis is on **clarity and traceability**: every reasoning step, tool invocation, and observation is visible and logged, making the agent’s behavior easy to follow and debug.

---

## Overview

The agent operates in a structured loop:
1. The model reasons about the problem step by step.
2. It decides whether a tool is required.
3. A tool is invoked if needed.
4. The result is added back into the conversation.
5. The loop continues until a clear stop condition is reached.

This simulates context-aware, tool-augmented reasoning without relying on external orchestration libraries.

---

## Agent Capabilities

The agent can:
- Solve **mathematical expressions** using safe evaluation and SymPy
- Perform **unit conversions** (length, weight, temperature)
- Compute **factorials**
- Route tool calls using a custom `TOOL:` format
- Parse and execute tool calls using **regex-based dispatch**
- Maintain a controlled reasoning loop with explicit termination logic

---

## Architecture

- **ReAct-style loop** (Reason → Act → Observe)
- Explicit tool routing and execution
- Tool results appended back into conversation context
- Clear separation between:
  - reasoning
  - tool execution
  - response generation

No hidden abstractions or framework-managed state.

---

## Built With

- **Python** – tool functions and controller logic  
- **Streamlit** – chat UI and session state management  
- **Groq API (LLaMA 3)** – step-by-step reasoning and decision-making  
- **SymPy** – symbolic math fallback  
- **Regex** – parsing and routing tool calls  
- **Thought logging** – expandable, step-by-step reasoning trace  

---

## Features

- Framework-free agent implementation
- Transparent reasoning and tool usage
- Safe expression evaluation and error handling
- Expandable reasoning trace in the UI
- Minimal and modular design

---

## Skills Applied & Strengthened

- ReAct prompting (Reason + Act)
- Tool usage via structured chat context
- Regex-based function routing
- Context-aware tool invocation
- Safe evaluation strategies
- Building controllable reasoning loops

---

## Scope & Notes

- This project is intended for **learning and experimentation**
- Not designed as a general-purpose agent framework
- Focuses on correctness, interpretability, and control rather than scale

---

## License

This project is released under the **MIT License**.  
You are free to use, modify, and distribute the code with proper attribution.
