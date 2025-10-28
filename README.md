# Generate-SPPU-Tech-Quiz

This repository contains LangFlow flows that generate 10 multiple-choice quizzes (MCQs) from subject content stored in Astra DB → https://astra.datastax.com

# Quiz Generator with LangFlow

Create auto-generated multiple-choice quizzes (MCQs) based on SPPU syllabus content using a no-code/low-code GenAI pipeline in LangFlow.

# 🎯 Project Goal

Build a GenAI pipeline that:

- Ingests Colud computing  textbooks into Astra DB  
- Retrieves relevant unit-wise content  
- Generates validated multiple-choice quiz questions with correct answers  

# Key Features

- Syllabus-driven quiz generation → Questions come directly from SPPU content  
- Unit-wise selection → Generate quizzes for any Unit (I–VI)  
- Configurable question count → Decide how many questions you want  
- Exam-oriented → Matches SPPU question patterns  
- Extendable → Replace SPPU subject with any other topic  

# Architecture (Flow Overview)

**Ingest Flow (quiz_ingest.json)**  
text book  Content → Split Text → Astra DB (storage)  

**Retrieve Flow (quiz_retrieve.json)**  
Chat Input → Astra DB → Parser → Prompt Template → Groq LLM → Chat Output  

# Components Used in LangFlow

- **Input:** User’s subject text or quiz request  
- **Astra DB:** Stores SPPU content chunks  
- **Parser:** Enforces schema & structure  
- **Prompt Template:** Custom instructions to generate MCQs  
- **LLM:** Groq (can be swapped with other LLMs)  
- **Output:** Display quiz with answers  

# Tech Stack

- LangFlow (flow orchestration)  
- Astra DB (vector DB for context storage & retrieval)  
- Groq LLM (for question generation)  
- Python 3.12.1  

#  Example Quiz Output

**Quiz: “Cloud Computing – Unit I”**

---

### 1. What is the main advantage of cloud computing?

A. Local storage  
B. On-demand resource availability  
C. Slow data processing  
D. Manual software installation  

---

### 2. Which model allows users to access hardware resources virtually?

A. SaaS  
B. PaaS  
C. IaaS  
D. DaaS  

---

### 3. Which cloud deployment type is owned by a single organization?

A. Public Cloud  
B. Private Cloud  
C. Hybrid Cloud  
D. Community Cloud  

---

##  Answers

| # | Correct Answer |
|---|----------------|
| 1 | **B** |
| 2 | **C** |
| 3 | **B** |

---

##  Score Card

| Score | Result |
|-------|--------|
| 5/5 | **Cloud Guru** – You’ve mastered the cloud concepts! |
| 4/5 | **Cloud Practitioner** – Almost perfect, just a minor gap. |
| 3/5 | **Cloud Explorer** – Good job, keep revising the units. |
| 2/5 | **Cloud Learner** – Need more practice, revisit the notes. |
| 1/5 | **Cloud Novice** – Start from basics and try again. |
| 0/5 | **Lost in the Clouds** – Time to study the units carefully. |

---

 Good luck, future tech wizard! 

# LangFlow Flow Architecture


This flow takes  content files, splits them into chunks, and ingests them into Astra DB.

### Ingest Flow!
<img width="1262" height="487" alt="image" src="https://github.com/user-attachments/assets/a783e4ac-8ef5-45b8-8edf-42e73c79f9e0" />


### Retrieve & Quiz Flow
This flow retrieves relevant content and generates quiz questions using Groq LLM.

<img width="1366" height="588" alt="image" src="https://github.com/user-attachments/assets/d584b9c7-7144-4625-be16-c90472fbce1d" />

---

### Example Output in Playground
Here’s how the generated quiz looks when displayed in LangFlow’s Playground:

<img width="1813" height="867" alt="image"  src="https://github.com/user-attachments/assets/ed99ab93-14f7-4155-8215-542a653b400f" />

### Here is the Scoring method for each student
Here’s how the Scores are shown in the end for a better understanding and overview:

<img width="1813" height="867" alt="image"  src="https://github.com/user-attachments/assets/6fd65e33-0b8b-41b3-8f9c-56bf5e0e3b6a" />


---

