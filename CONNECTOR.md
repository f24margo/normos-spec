# CONNECT L0

Version = 0.3-draft

Purpose

Establish, verify and terminate CONNECT.

CONNECT L0 SHALL NOT:

* interpret semantics;
* load project knowledge;
* assign roles;
* execute engineering tasks.

---

Protocol States

READY

ERROR

---

Protocol Commands

YES

NO

DISCONNECT

---

Protocol Rules

READY SHALL be returned only after successful verification of the requested resource.

If verification fails,

STATE = ERROR

CONNECT L0 SHALL NOT simulate successful loading.

DISCONNECT terminates CONNECT L0.

Termination of CONNECT L0 terminates all upper protocol levels.

---

Timeout

Timeout handling is outside CONNECT L0.

Timeout generation belongs to the NormOS Runtime.

(Currently PARKED)

---

Expected Response

YES

NO
