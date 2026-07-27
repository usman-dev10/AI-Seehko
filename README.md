# AI-Seehko

> Personal learning notes and session documentation from the **AI-Seehko** program — exploring AI prompting, assistants, language models, and foundational software engineering concepts.

---

## About

| | |
|---|---|
| **Author** | Muhammad Usman |
| **Role** | Student |
| **Program** | AI-Seehko Sessions |
| **Status** | Session 1 — First Class |

This repository documents key concepts, discussions, and takeaways from each AI-Seehko session. It serves as a structured reference for AI fundamentals and practical development practices learned in class.

---

## Session 1 — First Class

### 1. AI Prompting

Effective prompts are built around **four core components**:

| Component | Description |
|-----------|-------------|
| **Role** | Define who the AI should act as (e.g., teacher, coder, analyst). Sets tone and expertise level. |
| **Context** | Provide background information the AI needs to understand the situation. |
| **Main** | State the primary task, question, or goal clearly and directly. |
| **Conclusion** | Specify the desired output format, length, or closing instruction. |

> A well-structured prompt combining all four components produces more accurate, relevant, and useful AI responses.

---

### 2. AI Assistants

Discussion covered what **AI assistants** are and how they work in practice:

- Interactive tools powered by large language models
- Designed to help with writing, coding, research, and problem-solving
- Respond to natural language input and adapt based on conversation context
- Examples include ChatGPT, Cursor, GitHub Copilot, and similar platforms

---

### 3. LLM — Large Language Models

Introduction to **Large Language Models (LLMs)**:

- Deep learning models trained on vast amounts of text data
- Predict and generate human-like language based on input prompts
- Power most modern AI assistants and generative AI applications
- Examples: GPT, Claude, Gemini, LLaMA

---

### 4. Code Structure & Fundamentals

#### Directory Navigation

Essential commands for working with folders in the terminal:

| Command | Action |
|---------|--------|
| `cd .` | Stay in the current directory |
| `cd ..` | Move up one level to the parent directory |
| `mkdir <name>` | Create a new directory (folder) |

#### Modularity

- Break code into **small, independent, reusable modules**
- Each module handles one responsibility
- Improves readability, maintainability, and team collaboration
- Easier to test and debug individual parts without affecting the whole system

#### Redundancy

- **Redundancy** means repeating the same logic or data in multiple places
- Leads to harder maintenance — a change in one place requires changes everywhere
- Good code minimizes redundancy through functions, components, and shared utilities
- DRY principle: **Don't Repeat Yourself**

---

### 5. Linting & TypeScript

Discussion on **linting** and how **TypeScript** improves JavaScript development:

- **Linting** — Automated analysis that detects errors, bugs, and style issues in code before runtime
- Helps maintain consistent code quality across a project
- **TypeScript** — A superset of JavaScript that adds **static type checking**
- Catches type-related errors at compile time rather than at runtime
- Reduces bugs and improves developer experience in large codebases

```
JavaScript  →  Dynamic types, flexible but error-prone
TypeScript  →  Static types, catches errors early via linting & type checks
```

---

### 6. Programming Language Speed Comparison

Discussion on relative **execution speed** of popular languages:

| Rank | Language | Notes |
|------|----------|-------|
| 1 | **C++** | Fastest — compiled, low-level memory control |
| 2 | **JavaScript** | Moderate — interpreted/JIT compiled, runs in browsers & Node.js |
| 3 | **Python** | Slower — interpreted, prioritizes readability over raw speed |

> Speed is not the only factor when choosing a language. Developer productivity, ecosystem, and use case matter equally.

---

## Key Takeaways

- Structure AI prompts with **Role, Context, Main, and Conclusion** for better results
- **AI assistants** and **LLMs** are the foundation of modern generative AI tools
- Write **modular**, **non-redundant** code organized with clear directory structure
- Use **linting** and **TypeScript** to catch errors early in JavaScript projects
- Choose programming languages based on the problem, not just speed

---

## Repository Structure

```
AI-Seehko/
├── README.md          # Session notes and documentation
└── (future sessions will be added here)
```

---

## Author

**Muhammad Usman**  
Student — AI-Seehko Program

---

## License

This project is for personal educational use as part of the AI-Seehko learning program.

---

*Last updated: Session 1 — First Class*
