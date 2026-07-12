# NKS-003 — CONNECT Runtime

**Status:** Draft v0.1

---

# 1. Purpose

CONNECT Runtime executes the CONNECT L0 protocol.

This specification defines protocol behaviour.

Protocol rules remain defined by NKS-002-CONNECT-L0.

---

# 2. Responsibilities

CONNECT Runtime SHALL:

* maintain CONNECT L0 state;
* maintain the inactivity timer;
* detect timeout;
* generate DISCONNECT events;
* terminate all active upper protocol levels.

CONNECT Runtime SHALL NOT:

* interpret semantics;
* assign roles;
* analyse project content.

---

# 3. Runtime Parameters

## Default Timeout

```
DEFAULT_TIMEOUT = 10 min
```

## Allowed Timeout Values

```
10 min
20 min
30 min
```

No other timeout values are valid.

---

# 4. Runtime States

```
READY

DISCONNECTED
```

---

# 5. Runtime Events

```
CONNECT

TIMEOUT

DISCONNECT
```

---

# 6. Runtime Behaviour

## CONNECT

Initializes CONNECT L0.

Starts inactivity timer.

Enters READY state.

---

## Activity

Every valid CONNECT L0 interaction resets the inactivity timer.

---

## TIMEOUT

When inactivity timer expires:

* Runtime SHALL generate DISCONNECT.
* CONNECT L0 SHALL terminate.
* All upper protocol levels SHALL terminate.

---

## DISCONNECT

DISCONNECT immediately terminates:

* CONNECT L0
* L1
* L2
* L3
* all active upper protocol levels.

---

# 7. Dependencies

This Runtime executes:

```
NKS-002-CONNECT-L0
```

---

# 8. Conformance

A CONNECT Runtime implementation conforms to this specification only if it satisfies all SHALL requirements defined in this document.
