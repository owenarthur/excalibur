---
name: "begin_working"
description: "Queue a background working and return immediately."
---
Queue one durable working and return control to the foreground thread.

The working should receive a durable identity before its runner begins. A full implementation should record its purpose, authority, claimant, lease, checkpoints, and eventual terminal state without hiding them inside the provider process.

This scaffold keeps only the descriptive `spell.md` layer and omits the handler and runtime code.
