# Prompt Engineering & Generative AI Laboratory

[![Regulation](https://img.shields.io/badge/Regulation-ACETR23-blue.svg)](https://acet.ac.in)
[![Course](https://img.shields.io/badge/Course-AI%20%26%20Machine%20Learning-orange.svg)](#)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://python.org)
[![Node.js](https://img.shields.io/badge/Node.js-v20%2B%20%7C%20v22%2B-green.svg)](https://nodejs.org)
[![LLM](https://img.shields.io/badge/Model-Gemini%202.5%20Flash%20%7C%20LLaVA-purple.svg)](https://ai.google.dev/)
[![Deep Learning](https://img.shields.io/badge/Framework-PyTorch%20%7C%20LangChain-red.svg)](https://pytorch.org)

> **Aditya College of Engineering & Technology (ACET) — Regulation ACETR23**  
> **Department of Artificial Intelligence & Machine Learning**  
> A comprehensive, production-grade laboratory repository implementing the complete lifecycle of **Prompt Engineering**, **Chain-of-Thought Reasoning**, **LCEL Pipelines**, **Retrieval-Augmented Generation (RAG)**, **Autonomous ReAct Agents**, **Multimodal Vision-Language Systems**, and **Deep Generative Architectures**.

---

## 📑 Table of Contents

- [Overview & Architecture](#-overview--architecture)
- [Master Experiments Directory (01 – 22)](#-master-experiments-directory-01--22)
- [Curriculum Phases & Thematic Modules](#-curriculum-phases--thematic-modules)
  - [Phase I: Foundations & Persona Steering (Exp 01 - 07)](#phase-i-foundations--persona-steering-exp-01---07)
  - [Phase II: Structured Formatting & Declarative Chains (Exp 08 - 11)](#phase-ii-structured-formatting--declarative-chains-exp-08---11)
  - [Phase III: Retrieval-Augmented Generation & Agentic Systems (Exp 12 - 14)](#phase-iii-retrieval-augmented-generation--agentic-systems-exp-12---14)
  - [Phase IV: Multimodal Vision, Safety, Deep Learning & Audio (Exp 15 - 22)](#phase-iv-multimodal-vision-safety-deep-learning--audio-exp-15---22)
- [Individual Experiment Specifications](#-individual-experiment-specifications)
- [Prerequisites & Installation](#-prerequisites--installation)
- [Port Allocation Matrix](#-port-allocation-matrix)
- [Quick Start Guide](#-quick-start-guide)
- [Troubleshooting & FAQs](#-troubleshooting--faqs)

---

## 🏛 Overview & Architecture

Every experiment in this repository is architected with a **dual-execution paradigm**:
1. **Interactive Full-Stack Web Application**: Powered by **Node.js + Express** serving modern glassmorphism responsive user interfaces with real-time API integrations, telemetry metrics, and parameter sliders.
2. **Standalone Python Verification Engine**: Standalone, reproducible Python test scripts for programmatic evaluation, automated scoring, parameter testing, and command-line execution.

```mermaid
graph TD
    User([User / Browser]) <--> |HTTP / JSON (Ports 3000-3021)| Express[Express.js Web Server]
    Express <--> |Google GenAI SDK| GeminiAPI[Google Gemini 2.5 Flash API]
    Express <--> |In-Memory / PDF Parser| VectorStore[Vector Embedding / Indexing Engine]
    
    subgraph "Python Core & Deep Learning Backends"
        PythonCLI[Standalone Python Scripts] --> PyTorch[PyTorch / Torchvision Models]
        PythonCLI --> LangChain[LangChain / LCEL Runnables]
        PythonCLI --> LocalOllama[Ollama LLaVA Vision Server]
        PythonCLI --> GeminiPython[Google Generative AI Python SDK]
    end
```

---

## 📊 Master Experiments Directory (01 – 22)

| # | Experiment Folder | Module / Topic | Primary Tech Stack | Default Port | Standalone Script |
|:---:|:---|:---|:---|:---:|:---|
| **01** | `01_Environment_Setup` | Gemini AI API Connectivity & Credentials Setup | Gemini 2.5 Flash, Express, Dotenv | `3000` | `experiment1.py` |
| **02** | `02_Baseline_vs_Enhanced` | Baseline vs. Engineered Prompts (Persona & Framing) | Gemini API, Prompt Anatomy | `3001` | `experiment2.py` |
| **03** | `03_Iterative_Refinement` | 3-Round Iterative Prompt Optimization Lifecycle | Boundary Constraints, Density Scoring | `3002` | `experiment3.py` |
| **04** | `04_Prompt_Failures` | Diagnosing Prompt Pitfalls, Failures & Auto-Remediation | Failure Mode Classifier, Scoring | `3003` | `experiment4.py` |
| **05** | `05_FewShot_vs_ZeroShot` | Few-Shot Exemplars vs. Zero-Shot Inference | Exemplar Guidance, Format Alignment | `3004` | `experiment5.py` |
| **06** | `06_Role_Negative_Prompting` | Persona Steering & Content Suppression (Negative Constraints) | Brand/Ad Suppression, Tone Adherence | `3005` | `experiment6.py` |
| **07** | `07_Constraint_Refinement` | Constraint Specification & Rule Adherence Benchmarking | Word Limits, Negative Rules, Scoring | `3006` | `experiment7.py` |
| **08** | `08_Structured_Format` | Markdown Tables, Structured Bullet Lists & Regex Validation | Schema Parsing, Marked.js | `3007` | `experiment8.py` |
| **09** | `09_JSON_YAML_Generation` | Validated JSON/YAML Generation & Self-Correction Loops | JS-YAML, Auto-Refinement Loop | `3008` | `experiment9.py` |
| **10** | `10_Chain_of_Thought` | Chain-of-Thought (CoT) & Multi-Stage Task Decomposition | Step-by-Step Reasoning, Logic Verification | `3009` | `experiment10.py` |
| **11** | `11_LCEL_Chain` | LangChain Expression Language (LCEL) Declarative Pipeline | `@langchain/core`, Runnable Sequence | `3010` | `experiment11.py` |
| **12** | `12_RAG_Retrieval` | Document Ingestion, Semantic Chunking & Cosine Vector Indexing | PDF-Parse, Text Embeddings, Math Cosine | `3011` | `experiment12.py` |
| **13** | `13_Conversational_RAG` | End-to-End Conversational RAG with Context Grounding | Vector Retrieval, Context Injection, Multi-Turn | `3012` | `experiment13.py` |
| **14** | `14_ReAct_Agent` | Autonomous ReAct Agent with Tool Invocation (AST Math & Unit) | Safe AST Calculator, Tool Dispatcher | `3013` | `experiment14.py` |
| **15** | `15_Multimodal_Vision` | Multimodal Vision Prompting (VQA, Captioning & Telemetry) | Multer, Vision Gemini Models | `3014` | `experiment15.py` |
| **16** | `16_Evaluation_Ethics` | Prompt Evaluation, LLM-as-a-Judge & Injection Defense | Delimiter Sandboxing, 4-Metric Judge | `3015` | `experiment16.py` |
| **17** | `17_CNN_CIFAR10` | Deep Convolutional Neural Network (CNN) 10-Class Classifier | PyTorch, BatchNorm, Dropout, Softmax | `3016` | `experiment17.py` |
| **18** | `18_Style_Transfer` | Neural Style Transfer (NST) using Deep Feature Optimizations | PyTorch, VGG19, Gram Matrix Loss | `3017` | `experiment18.py` |
| **19** | `19_VQA_LLaVA` | Visual Question Answering using Ollama LLaVA Local Model | Ollama HTTP API, LLaVA 7B Vision | `3018` | `experiment19.py` |
| **20** | `20_Video_Analyzer` | Spatiotemporal Video Action Recognition & Scene Summarization | Video Keyframe Extraction, Transformers | `3019` | `experiment20.py` |
| **21** | `21_Music_Generation` | Polyphonic Multi-Track Algorithmic & Generative Music (MuseGAN) | PyTorch Generative Latents, Multi-Track Audio | `3020` | `experiment21.py` |
| **22** | `22_Voice_STT_TTS` | Multimodal Voice AI System (Speech-to-Text & Text-to-Speech) | Web Speech API, Audio Synthesis, Gemini | `3021` | `experiment22.py` |

---

## 🎯 Curriculum Phases & Thematic Modules

### Phase I: Foundations & Persona Steering (Exp 01 - 07)
- **Exp 01 (Environment Setup)**: Establishing API handshake, securely loading environment variables, validating rate limits and model status.
- **Exp 02 (Baseline vs Enhanced)**: Dissecting naive input queries versus systematically engineered prompts with audience framing, role assignment, and contextual delimiters.
- **Exp 03 (Iterative Refinement)**: Tracking the iterative prompt engineering lifecycle through multiple refinement passes to optimize keyword density and adherence.
- **Exp 04 (Prompt Failures)**: Root cause analysis of prompt vulnerabilities (vagueness, opposing constraints, lack of context) with automatic remediation synthesis.
- **Exp 05 (Few-Shot vs. Zero-Shot)**: Quantifying the gain in schema stability and output consistency provided by structured exemplar demonstrations.
- **Exp 06 (Role & Negative Prompting)**: Enforcing strict domain personas while suppressing non-compliant entities, commercial noise, and tangential output.
- **Exp 07 (Constraint Refinement)**: Benchmarking output adherence against strict length ceilings, format boundaries, and negative rule sets.

### Phase II: Structured Formatting & Declarative Chains (Exp 08 - 11)
- **Exp 08 (Structured Format)**: Directing models to synthesize Markdown tabular representations and bulleted hierarchies, validated by deterministic regex parsers.
- **Exp 09 (JSON & YAML Generation)**: Programmatic syntax verification and self-healing refinement loops for machine-readable payloads.
- **Exp 10 (Chain-of-Thought)**: Multi-step reasoning decomposition, zero-shot "Think step-by-step" guidance, and logical error minimization on mathematical puzzles.
- **Exp 11 (Simple LCEL Chain)**: Implementing LangChain Expression Language (LCEL) declarative composition (`PromptTemplate | ChatModel | StrOutputParser`).

### Phase III: Retrieval-Augmented Generation & Agentic Systems (Exp 12 - 14)
- **Exp 12 (RAG Data Indexing)**: PDF ingestion, sliding-window chunking (500 chars with 50 char overlap), dense vector embedding generation, and cosine similarity indexing.
- **Exp 13 (Conversational RAG Chain)**: Production conversational retrieval pipeline with citation grounding, multi-turn history, and hallucination reduction.
- **Exp 14 (Autonomous ReAct Agent)**: Dynamic Tool Execution framework operating on a Reason + Act loop, integrating an Abstract Syntax Tree (AST) mathematical evaluator and unit conversion engine.

### Phase IV: Multimodal Vision, Safety, Deep Learning & Audio (Exp 15 - 22)
- **Exp 15 (Multimodal Prompting)**: Dual-stream visual reasoning: scene captioning, visual question answering, and structured telemetry extraction from image buffers.
- **Exp 16 (Evaluation & Ethics)**: Automated LLM-as-a-Judge across 4 orthogonal dimensions (Relevance, Factuality, Safety, Clarity) alongside defensive sandboxing against prompt injections.
- **Exp 17 (CNN CIFAR-10 Classification)**: Convolutional neural network classification across 10 object classes featuring feature maps, batch normalization, and test evaluation.
- **Exp 18 (Neural Style Transfer)**: Deep convolutional optimization combining photographic content with artistic style through Gatys et al. Gram matrix loss minimization.
- **Exp 19 (Ollama LLaVA VQA)**: Local open-weights vision-language deployment using Ollama and LLaVA for private, on-device image interrogation.
- **Exp 20 (Video Scene Analyzer)**: Keyframe extraction, spatiotemporal action recognition, and temporal segment summarization for video streams.
- **Exp 21 (MuseGAN Multi-Track Music)**: Synthesizing multi-instrument polyphonic musical arrangements (Piano, Bass, Drums) via coordinated deconvolutional networks.
- **Exp 22 (Voice STT & TTS Multimodal System)**: Complete hands-free conversational voice assistant combining real-time Speech Recognition, LLM reasoning, and natural Text-to-Speech synthesis.

---

## 🔍 Individual Experiment Specifications

### 01_Environment_Setup
- **Directory**: `01_Environment_Setup/`
- **Port**: `3000`
- **Files**: `server.js`, `experiment1.py`, `public/index.html`, `public/app.js`, `public/style.css`
- **Summary**: Validates connectivity to Google Gemini API (`gemini-2.5-flash`), tests token retrieval from `.env`, and displays real-time latency and connection telemetry.
- **Run Server**:
  ```bash
  cd 01_Environment_Setup
  npm start
  ```
- **Run Python**:
  ```bash
  python 01_Environment_Setup/experiment1.py
  ```

---

### 02_Baseline_vs_Enhanced
- **Directory**: `02_Baseline_vs_Enhanced/`
- **Port**: `3001`
- **Files**: `server.js`, `experiment2.py`, `public/`
- **Summary**: Provides an interactive side-by-side comparison between an unguided baseline prompt and an engineered prompt with persona, target audience, structural constraints, and quality metrics.
- **Run Server**:
  ```bash
  cd 02_Baseline_vs_Enhanced
  npm start
  ```
- **Run Python**:
  ```bash
  python 02_Baseline_vs_Enhanced/experiment2.py
  ```

---

### 03_Iterative_Refinement
- **Directory**: `03_Iterative_Refinement/`
- **Port**: `3002`
- **Files**: `server.js`, `experiment3.py`, `public/`
- **Summary**: Simulates a 3-cycle iterative prompt refinement loop. Computes character count, word density, and rule compliance score across progressive passes.
- **Run Server**:
  ```bash
  cd 03_Iterative_Refinement
  npm start
  ```
- **Run Python**:
  ```bash
  python 03_Iterative_Refinement/experiment3.py
  ```

---

### 04_Prompt_Failures
- **Directory**: `04_Prompt_Failures/`
- **Port**: `3003`
- **Files**: `server.js`, `experiment4.py`, `experiment4_record.py`, `streamlit_app.py`, `app.py`, `public/`
- **Summary**: Diagnoses 4 common prompt failure modes: Contradictory constraints, Ambiguous scope, Missing format, and Underspecified context. Automatically generates an optimized, failure-free replacement prompt.
- **Run Server**:
  ```bash
  cd 04_Prompt_Failures
  npm start
  ```
- **Run Python**:
  ```bash
  python 04_Prompt_Failures/experiment4.py
  ```

---

### 05_FewShot_vs_ZeroShot
- **Directory**: `05_FewShot_vs_ZeroShot/`
- **Port**: `3004`
- **Files**: `server.js`, `experiment5.py`, `tkinter_app.py`, `public/`
- **Summary**: Demonstrates the impact of in-context learning by executing a Zero-Shot prompt alongside a 3-Exemplar Few-Shot prompt. Displays output consistency, format adherence, and token efficiency.
- **Run Server**:
  ```bash
  cd 05_FewShot_vs_ZeroShot
  npm start
  ```
- **Run Python**:
  ```bash
  python 05_FewShot_vs_ZeroShot/experiment5.py
  ```

---

### 06_Role_Negative_Prompting
- **Directory**: `06_Role_Negative_Prompting/`
- **Port**: `3005`
- **Files**: `server.js`, `experiment6.py`, `public/`
- **Summary**: Evaluates role-based persona steerability (e.g. Senior Cybersecurity Auditor, Pediatrician) combined with negative prompting to ban promotional words, specific brand names, and extraneous conversational preamble.
- **Run Server**:
  ```bash
  cd 06_Role_Negative_Prompting
  npm start
  ```
- **Run Python**:
  ```bash
  python 06_Role_Negative_Prompting/experiment6.py
  ```

---

### 07_Constraint_Refinement
- **Directory**: `07_Constraint_Refinement/`
- **Port**: `3006`
- **Files**: `server.js`, `experiment7.py`, `public/`
- **Summary**: Applies strict multi-layered constraints (exact word count bounds, bullet format requirements, required keywords, and prohibited topics) and evaluates compliance percentage in real time.
- **Run Server**:
  ```bash
  cd 07_Constraint_Refinement
  npm start
  ```
- **Run Python**:
  ```bash
  python 07_Constraint_Refinement/experiment7.py
  ```

---

### 08_Structured_Format
- **Directory**: `08_Structured_Format/`
- **Port**: `3007`
- **Files**: `server.js`, `experiment8.py`, `experiment8_record.py`, `public/`
- **Summary**: Mandates structured output formats (Markdown tables with predefined columns and bulleted operational checklists). Validates markdown structure with client-side and server-side parsers.
- **Run Server**:
  ```bash
  cd 08_Structured_Format
  npm start
  ```
- **Run Python**:
  ```bash
  python 08_Structured_Format/experiment8.py
  ```

---

### 09_JSON_YAML_Generation
- **Directory**: `09_JSON_YAML_Generation/`
- **Port**: `3008`
- **Files**: `server.js`, `experiment9.py`, `public/`
- **Summary**: Generates strictly valid JSON and YAML outputs according to a specified schema. Features an automated recovery loop that detects syntax errors and prompts the LLM for self-correction.
- **Run Server**:
  ```bash
  cd 09_JSON_YAML_Generation
  npm start
  ```
- **Run Python**:
  ```bash
  python 09_JSON_YAML_Generation/experiment9.py
  ```

---

### 10_Chain_of_Thought
- **Directory**: `10_Chain_of_Thought/`
- **Port**: `3009`
- **Files**: `server.js`, `experiment10.py`, `public/`
- **Summary**: Contrasts standard direct prompting against Zero-Shot Chain-of-Thought ("Think step by step") and explicit multi-stage task decomposition on complex logic and arithmetic benchmarks.
- **Run Server**:
  ```bash
  cd 10_Chain_of_Thought
  npm start
  ```
- **Run Python**:
  ```bash
  python 10_Chain_of_Thought/experiment10.py
  ```

---

### 11_LCEL_Chain
- **Directory**: `11_LCEL_Chain/`
- **Port**: `3010`
- **Files**: `server.js`, `experiment11.py`, `public/`
- **Summary**: Builds a declarative LangChain Expression Language (LCEL) pipeline: `PromptTemplate | ChatModel | StrOutputParser`. Allows customization of prompt templates and model temperature dynamically.
- **Run Server**:
  ```bash
  cd 11_LCEL_Chain
  npm start
  ```
- **Run Python**:
  ```bash
  python 11_LCEL_Chain/experiment11.py
  ```

---

### 12_RAG_Retrieval
- **Directory**: `12_RAG_Retrieval/`
- **Port**: `3011`
- **Files**: `server.js`, `experiment12.py`, `app.py`, `college-rules123.pdf`, `public/`
- **Summary**: Extracts text from PDF documents (`college-rules123.pdf`), splits content into 500-character chunks with 50-character overlap, generates vector representations, and runs cosine similarity retrieval for user queries.
- **Run Server**:
  ```bash
  cd 12_RAG_Retrieval
  npm start
  ```
- **Run Python**:
  ```bash
  python 12_RAG_Retrieval/experiment12.py
  ```

---

### 13_Conversational_RAG
- **Directory**: `13_Conversational_RAG/`
- **Port**: `3012`
- **Files**: `server.js`, `experiment13.py`, `college-rules123.pdf`, `public/`
- **Summary**: Complete Conversational Retrieval-Augmented Generation system. Retrieves relevant PDF chunks, injects them into the conversational context, tracks conversation history, and provides cited answers with source metadata.
- **Run Server**:
  ```bash
  cd 13_Conversational_RAG
  npm start
  ```
- **Run Python**:
  ```bash
  python 13_Conversational_RAG/experiment13.py
  ```

---

### 14_ReAct_Agent
- **Directory**: `14_ReAct_Agent/`
- **Port**: `3013`
- **Files**: `server.js`, `experiment14.py`, `public/`
- **Summary**: Implements a Reasoning + Acting (ReAct) autonomous agent. The model reasons through intermediate thoughts, invokes external tools (safe AST mathematical calculator and unit converter), and synthesizes a final verified answer.
- **Run Server**:
  ```bash
  cd 14_ReAct_Agent
  npm start
  ```
- **Run Python**:
  ```bash
  python 14_ReAct_Agent/experiment14.py
  ```

---

### 15_Multimodal_Vision
- **Directory**: `15_Multimodal_Vision/`
- **Port**: `3014`
- **Files**: `server.js`, `experiment15.py`, `sample_input.jpg`, `public/`
- **Summary**: Explores multimodal image understanding with Gemini Vision. Supports drag-and-drop image uploads for zero-shot image captioning, Visual Question Answering (VQA), and structured JSON telemetry extraction.
- **Run Server**:
  ```bash
  cd 15_Multimodal_Vision
  npm start
  ```
- **Run Python**:
  ```bash
  python 15_Multimodal_Vision/experiment15.py
  ```

---

### 16_Evaluation_Ethics
- **Directory**: `16_Evaluation_Ethics/`
- **Port**: `3015`
- **Files**: `server.js`, `experiment16.py`, `public/`
- **Summary**: Implements LLM-as-a-Judge scoring across 4 dimensions: **Relevance**, **Factuality**, **Safety**, and **Clarity** (1-5 scale). Includes prompt injection vulnerability testing and demonstrates delimiter sandboxing defense.
- **Run Server**:
  ```bash
  cd 16_Evaluation_Ethics
  npm start
  ```
- **Run Python**:
  ```bash
  python 16_Evaluation_Ethics/experiment16.py
  ```

---

### 17_CNN_CIFAR10
- **Directory**: `17_CNN_CIFAR10/`
- **Port**: `3016`
- **Files**: `server.js`, `experiment17.py`, `public/`
- **Summary**: 3-stage Deep Convolutional Neural Network with Batch Normalization, Dropout, and Max Pooling trained/evaluated on the 10-class CIFAR-10 image taxonomy (airplane, car, bird, cat, deer, dog, frog, horse, ship, truck).
- **Run Server**:
  ```bash
  cd 17_CNN_CIFAR10
  npm start
  ```
- **Run Python**:
  ```bash
  python 17_CNN_CIFAR10/experiment17.py
  ```

---

### 18_Style_Transfer
- **Directory**: `18_Style_Transfer/`
- **Port**: `3017`
- **Files**: `server.js`, `experiment18.py`, `content_city.jpg`, `style_starry.jpg`, `stylized_result.jpg`, `public/`
- **Summary**: Implements Neural Style Transfer (Gatys et al.) using PyTorch and deep VGG convolutional representations. Jointly minimizes content loss and Gram matrix style loss to blend photographs with artwork styles.
- **Run Server**:
  ```bash
  cd 18_Style_Transfer
  npm start
  ```
- **Run Python**:
  ```bash
  python 18_Style_Transfer/experiment18.py
  ```

---

### 19_VQA_LLaVA
- **Directory**: `19_VQA_LLaVA/`
- **Port**: `3018`
- **Files**: `server.js`, `experiment19.py`, `sample_image.jpg`, `public/`
- **Summary**: Visual Question Answering using local open-source LLaVA (Large Language and Vision Assistant) via Ollama with automatic fallback to Gemini Vision. Performs detailed spatial and semantic scene analysis.
- **Run Server**:
  ```bash
  cd 19_VQA_LLaVA
  npm start
  ```
- **Run Python**:
  ```bash
  python 19_VQA_LLaVA/experiment19.py
  ```

---

### 20_Video_Analyzer
- **Directory**: `20_Video_Analyzer/`
- **Port**: `3019`
- **Files**: `server.js`, `experiment20.py`, `video_frame.jpg`, `public/`
- **Summary**: Video action recognition and temporal event summarization using spatiotemporal visual understanding. Generates chronological event timelines, keyframe descriptions, and answers questions about dynamic scenes.
- **Run Server**:
  ```bash
  cd 20_Video_Analyzer
  npm start
  ```
- **Run Python**:
  ```bash
  python 20_Video_Analyzer/experiment20.py
  ```

---

### 21_Music_Generation
- **Directory**: `21_Music_Generation/`
- **Port**: `3020`
- **Files**: `server.js`, `experiment21.py`, `public/`
- **Summary**: Multi-track polyphonic music generation inspired by MuseGAN. Synthesizes synchronized tracks for Piano, Bass, and Drums with adjustable tempo, genre parameters, and interactive visual audio track players.
- **Run Server**:
  ```bash
  cd 21_Music_Generation
  npm start
  ```
- **Run Python**:
  ```bash
  python 21_Music_Generation/experiment21.py
  ```

---

### 22_Voice_STT_TTS
- **Directory**: `22_Voice_STT_TTS/`
- **Port**: `3021`
- **Files**: `server.js`, `experiment22.py`, `public/`
- **Summary**: End-to-end hands-free multimodal conversational AI. Captures acoustic speech using the Web Speech API (Speech-to-Text), streams query to Gemini, and synthesizes speech responses using Text-to-Speech (TTS) audio.
- **Run Server**:
  ```bash
  cd 22_Voice_STT_TTS
  npm start
  ```
- **Run Python**:
  ```bash
  python 22_Voice_STT_TTS/experiment22.py
  ```

---

## 💻 Prerequisites & Installation

### 1. System Requirements
- **Node.js**: `v20.x` or `v22.x` ([Download](https://nodejs.org))
- **Python**: `3.10.x` or `3.11.x` ([Download](https://www.python.org))
- **Operating System**: Windows 10/11, macOS, or Linux
- **Ollama (Optional, for Exp 19 LLaVA)**: [Ollama](https://ollama.com) (`ollama run llava`)

### 2. Global Environment Setup (.env)
A `.env` file is present in the root folder as well as in each individual experiment directory:

```env
GEMINI_API_KEY=your_google_gemini_api_key_here
```

> **Note**: Obtain a free Gemini API key from [Google AI Studio](https://aistudio.google.com/).

### 3. Install Python Dependencies
Install required Python packages across the lab:
```bash
pip install google-generativeai python-dotenv langchain-core langchain-google-genai pypdf torch torchvision pillow numpy
```

### 4. Install Node Dependencies
Each experiment directory includes its own `package.json` with pre-installed `node_modules`. If you ever need to reinstall dependencies in any experiment:
```bash
cd 01_Environment_Setup
npm install
```

---

## 🌐 Port Allocation Matrix

To prevent port conflicts and allow running multiple experiments concurrently, each experiment runs on a dedicated port:

```
Port 3000 -> Exp 01: Environment Setup
Port 3001 -> Exp 02: Baseline vs Enhanced
Port 3002 -> Exp 03: Iterative Refinement
Port 3003 -> Exp 04: Prompt Failures & Remediation
Port 3004 -> Exp 05: Few-Shot vs Zero-Shot
Port 3005 -> Exp 06: Role & Negative Prompting
Port 3006 -> Exp 07: Constraint Refinement
Port 3007 -> Exp 08: Structured Format (Tables & Lists)
Port 3008 -> Exp 09: JSON & YAML Generation
Port 3009 -> Exp 10: Chain of Thought (CoT)
Port 3010 -> Exp 11: Simple LCEL Chain
Port 3011 -> Exp 12: Basic RAG Retrieval
Port 3012 -> Exp 13: Conversational RAG Chain
Port 3013 -> Exp 14: Autonomous ReAct Agent
Port 3014 -> Exp 15: Multimodal Vision
Port 3015 -> Exp 16: Prompt Evaluation & Ethics
Port 3016 -> Exp 17: CNN CIFAR-10 Classification
Port 3017 -> Exp 18: Neural Style Transfer (NST)
Port 3018 -> Exp 19: Ollama LLaVA VQA
Port 3019 -> Exp 20: Video Analyzer
Port 3020 -> Exp 21: MuseGAN Music Generation
Port 3021 -> Exp 22: Voice STT / TTS Assistant
```

---

## 🚀 Quick Start Guide

### Running Any Web Application
Navigate to the desired experiment folder and start its server:
```powershell
cd 14_ReAct_Agent
npm start
```
Then open your web browser and navigate to:
```
http://localhost:3013
```

### Running Any Standalone Python Script
Execute the experiment script directly from terminal:
```powershell
python 14_ReAct_Agent/experiment14.py
```

### Running All Node Servers (PowerShell Helper)
If you wish to run a specific range of experiments concurrently in background jobs:
```powershell
# Example: Start Experiments 1 through 5
1..5 | ForEach-Object {
    $folder = Get-ChildItem -Directory -Filter ("0$($_)_*")
    Start-Process -FilePath "node" -ArgumentList "server.js" -WorkingDirectory $folder.FullName
}
```

---

## 🛠 Troubleshooting & FAQs

### 1. `Missing GEMINI_API_KEY`
- **Cause**: The `.env` file is missing or `GEMINI_API_KEY` is empty.
- **Fix**: Verify `.env` exists in the experiment directory or root folder and contains `GEMINI_API_KEY=AIzaSy...`.

### 2. `Port Already in Use (EADDRINUSE)`
- **Cause**: A previously launched node process is still occupying the port.
- **Fix**: Identify and terminate the occupying process:
  ```powershell
  # Find PID using port (e.g. 3013)
  Get-NetTCPConnection -LocalPort 3013 -ErrorAction SilentlyContinue | Select-Object OwningProcess
  # Stop the process
  Stop-Process -Id <PID> -Force
  ```

### 3. `ModuleNotFoundError: No module named 'google'`
- **Fix**: Install the official Google Generative AI Python SDK:
  ```bash
  pip install google-generativeai python-dotenv
  ```

### 4. `Ollama connection refused in Exp 19 (LLaVA)`
- **Cause**: Ollama daemon is not running locally.
- **Fix**: Start the Ollama application or run `ollama serve`. Exp 19 automatically falls back to Gemini Vision if Ollama is unreachable.

---

## 🎓 Academic Attribution & Acknowledgments

- **Institution**: Aditya College of Engineering & Technology (ACET)
- **Academic Regulation**: ACETR23
- **Laboratory**: Prompt Engineering & Generative Artificial Intelligence Laboratory
- **Models & APIs**: Google Gemini 2.5 Flash, LangChain, PyTorch, Ollama LLaVA
- **Documentation Standards**: IEEE / Academic Laboratory Manual specifications conforming to ACETR23 guidelines.
