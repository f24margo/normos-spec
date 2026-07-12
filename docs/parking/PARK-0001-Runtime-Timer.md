# PARK-0001

Title

Runtime Timer

Status

PARKED

Reason

NormOS Runtime does not yet exist.

Decision

CONNECT L0 does not measure time.

Timeout generation belongs to the NormOS Runtime.

Prerequisite

Kernel Runtime implementation.

Return Condition

Resume after Kernel Runtime MVP.

# Deferred Design Note — Runtime Timer

**Status:** DRAFT

**Priority:** After Kernel MVP

## Decision

CONNECT L0 does not measure time.

CONNECT L0 only reacts to protocol events.

## Runtime Responsibility

Timeout generation belongs to the NormOS Runtime.

The Runtime SHALL:

* maintain inactivity timers;
* generate TIMEOUT events;
* generate DISCONNECT after timeout expiration.

## Current Status

NormOS Runtime does not yet exist.

During Kernel MVP no timer implementation is required.

## Revisit Condition

Return to this design after completion of the Kernel Runtime.
