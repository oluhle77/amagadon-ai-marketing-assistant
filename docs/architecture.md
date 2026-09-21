# Amagadon Architecture

## AI Fluency Project

**Assistant:** Amagadon - AI Marketing Assistant  
**Owner:** Thandoluhle Hlatshwayo  
**Track:** Track B: Marketing  
**Platform:** Claude.ai Projects  
**Version:** Amagadon v1.4  
**Status:** Pilot Deployment Ready  

---

# 1. Overview

Amagadon is a specialised AI Marketing Assistant developed as part of the
AI Fluency Project for Track B: Marketing.

The primary use case is to transform:

- marketing topics
- blog briefs
- blog articles
- campaign briefs
- approved marketing information

into three platform-specific social media post variations for LinkedIn or
Instagram.

The default variations are:

1. Authority and Insight
2. Human and Conversational
3. Concise and Action-Oriented

Amagadon is designed as a human-in-the-loop assistant.

It creates marketing drafts but does not independently approve or publish
marketing content.

---

# 2. Architecture Overview

Amagadon uses two main configuration layers:

1. Project Instructions
2. Project Context

The user provides the marketing request.

The Project Instructions coordinate the workflow.

The Project Context provides the detailed marketing rules, reference
material and responsible-AI controls.

The resulting content is then presented for human review.

---

# 3. High-Level Architecture

```text
                    USER
                      |
                      v
              Marketing Request
                      |
                      v
              +---------------+
              |   AMAGADON    |
              |     v1.4      |
              +---------------+
                      |
          +-----------+-----------+
          |                       |
          v                       v
 +----------------+      +------------------+
 |  INSTRUCTIONS  |      | PROJECT CONTEXT  |
 +----------------+      +------------------+
 | Workflow       |      | Brand Voice      |
 | Clarification  |      | Social Rules     |
 | 3 Variations   |      | Marketing Facts  |
 | Fact Control   |      | Examples         |
 | Output Format  |      | AI Guardrails    |
 +----------------+      +------------------+
          |                       |
          +-----------+-----------+
                      |
                      v
              Brief Interpretation
                      |
                      v
        +-------------+-------------+
        |             |             |
        v             v             v
     OPTION 1      OPTION 2      OPTION 3
     Authority     Human         Concise
     & Insight     & Convers.    & Action
        |             |             |
        +-------------+-------------+
                      |
                      v
              Fact / Rule Check
                      |
                      v
               Human Review
                      |
                      v
             Approved Content
                      |
                      v
             Manual Publication
