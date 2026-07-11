# Engineering Experiment

Document ID: EXP-0001

Title: Connector Bootstrap Validation

Version: 0.1

Status: Completed

Category: Engineering Experiment

Date: 2026-07-11

---

# Purpose

Validate that different AI systems can initialize the NormOS project using only the PROJECT CONNECTOR.

The experiment evaluates whether CONNECTOR.md is sufficient to establish a common engineering context without additional explanations.

---

# Initial Conditions

Repository:

NormOS

Bootstrap document:

CONNECTOR.md

No additional project description was provided.

The AI received only the link to CONNECTOR.md.

---

# Tested AI Systems

- ChatGPT
- Gemini
- Grok

---

# Expected Behaviour

After reading CONNECTOR.md the AI should:

1. Load the project context.
2. Accept the project role.
3. Report READY.
4. Wait for an engineering task.
5. Ask clarifying questions instead of making assumptions.

---

# Results

## ChatGPT

Result:

CONNECTOR LOADED

STATUS = READY

Accepted project context.

Asked clarifying engineering questions.

---

## Gemini

Result:

CONNECTOR LOADED

STATUS = READY

ROLE = Full Stack Engineering Assistant

Waiting for engineering task.

Asked for the first engineering task.

---

## Grok

Result:

CONNECTOR LOADED

STATUS = READY

ROLE = Full Stack Engineering Assistant

Waiting for engineering task.

Asked for the first engineering task.

---

# Observations

The three AI systems demonstrated similar bootstrap behaviour.

The CONNECTOR successfully synchronized:

- project identity;
- engineering role;
- repository as the source of truth;
- transition into engineering dialogue.

No AI attempted to restart project analysis from scratch.

---

# Conclusions

The experiment confirms that CONNECTOR.md functions as an effective AI bootstrap protocol.

The current protocol is sufficient for initiating a consistent engineering session across multiple AI systems.

Future improvements should focus on:

- richer session initialization;
- verified workspace description;
- standardized bootstrap response;
- connector protocol evolution.

---

# Decision

Experiment EXP-0001 is accepted.

The CONNECTOR concept becomes a validated engineering component of the NormOS project.
