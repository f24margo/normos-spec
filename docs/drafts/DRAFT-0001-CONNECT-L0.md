# DRAFT-0001 — CONNECT L0

**Status:** DRAFT

**Purpose**

This document records the origin and evolution of the CONNECT L0 protocol.

It is not a normative specification.

Its purpose is to preserve engineering reasoning, accepted decisions and open questions before promotion to an NKS specification.

---

# Background

During development of NormOS it became evident that communication between a human and an AI requires a formally defined transport protocol.

The first objective is not interpretation of meaning.

The first objective is establishing and maintaining CONNECT.

This protocol was named **CONNECT L0**.

---

# Initial Principles

CONNECT L0 SHALL operate only with protocol states.

CONNECT L0 SHALL NOT:

* interpret semantics;
* assign engineering roles;
* analyse project content;
* execute engineering tasks.

These responsibilities belong to higher protocol levels.

---

# Accepted Decisions

## D-0001

CONNECT L0 is the foundation of the protocol stack.

All upper protocol levels depend on CONNECT L0.

Status: ACCEPTED

---

## D-0002

Every protocol interaction SHALL require acknowledgement from the second participant.

The protocol does not complete a transition until acknowledgement is received.

Status: ACCEPTED

---

## D-0003

The command interface is defined only by the repository specification.

The chat is not a command interface.

Status: ACCEPTED

---

## D-0004

Only predefined protocol tokens are treated as CONNECT L0 commands.

All other text is ordinary conversation.

Status: ACCEPTED

Current command vocabulary:

* YES
* NO
* TIMEOUT 10
* TIMEOUT 20
* TIMEOUT 30
* DISCONNECT

---

## D-0005

Default timeout value is 10 minutes.

Allowed timeout values:

* 10
* 20
* 30

Status: ACCEPTED

---

## D-0006

TIMEOUT causes DISCONNECT.

After DISCONNECT a new CONNECT L0 session is required.

Status: ACCEPTED

---

## D-0007

DISCONNECT of CONNECT L0 automatically terminates all active upper protocol levels.

L1

L2

L3

...

Status: ACCEPTED

---

## D-0008

Protocol definition and protocol execution are different concerns.

CONNECT L0 defines behaviour.

CONNECT Runtime executes behaviour.

Status: ACCEPTED

---

# Open Questions

OQ-0001

Formal definition of the CONNECT Runtime.

Status: OPEN

---

OQ-0002

Repository command that initiates a controlled DISCONNECT.

Status: OPEN

---

OQ-0003

Transition procedure from CONNECT L0 to CONNECT L1.

Status: OPEN

---

# Promotion Rule

This document is working memory.

Accepted concepts may later be promoted into normative specifications.

Promotion target:

NKS-002-CONNECT-L0

NKS-003-CONNECT-RUNTIME
