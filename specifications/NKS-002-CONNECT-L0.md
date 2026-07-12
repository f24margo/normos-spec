# NKS-002 — CONNECT L0

**Status:** Draft v0.1

---

# 1. Purpose

CONNECT L0 defines the minimum protocol required to establish, maintain and terminate CONNECT.

CONNECT L0 is the foundation of all higher protocol levels.

---

# 2. Scope

CONNECT L0 SHALL:

* establish CONNECT;
* maintain CONNECT;
* terminate CONNECT;
* exchange protocol acknowledgements.

CONNECT L0 SHALL NOT:

* interpret semantics;
* assign roles;
* analyse project content;
* execute engineering tasks.

---

# 3. Protocol States

* READY
* DISCONNECTED

---

# 4. Protocol Commands

## Response Commands

* YES
* NO

## Timeout Commands

* TIMEOUT 10
* TIMEOUT 20
* TIMEOUT 30

Default:

* TIMEOUT 10

## Termination Command

* DISCONNECT

No other commands are valid at CONNECT L0.

---

# 5. Normative Rules

### NKS-L0-001

CONNECT L0 SHALL be active before any higher protocol level.

---

### NKS-L0-002

Every protocol request SHALL expect an acknowledgement.

Allowed acknowledgements:

* YES
* NO

---

### NKS-L0-003

Only commands defined by this specification SHALL modify CONNECT L0 state.

Any other text SHALL be treated as ordinary conversation.

---

### NKS-L0-004

TIMEOUT SHALL terminate CONNECT L0.

---

### NKS-L0-005

DISCONNECT SHALL terminate CONNECT L0.

---

### NKS-L0-006

Termination of CONNECT L0 SHALL automatically terminate all active upper protocol levels.

---

### NKS-L0-007

A new session SHALL begin with a new CONNECT L0.

---

# 6. Runtime

Execution of this protocol is defined by:

NKS-003-CONNECT-RUNTIME

---

# 7. Conformance

An implementation conforms to CONNECT L0 only if all SHALL requirements defined in this specification are satisfied.
