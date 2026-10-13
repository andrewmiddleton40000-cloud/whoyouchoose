---
name: Preview-generated Replit metadata
description: Replit preview setup may rewrite generated runtime modules and port mappings in imported projects.
---

In this imported static-site project, starting a temporary local preview caused Replit to update `.replit` with web, Python, and Node modules plus a port mapping. A supported attempt to restore the original file was followed by another artifact-metadata update that reintroduced the preview settings.

**Why:** The preview environment can synchronize its generated metadata independently of application-source edits.

**How to apply:** When preview-related `.replit` changes appear, confirm whether they are generated before treating them as intentional project configuration. Use the supported Replit configuration flow for persistent run behavior rather than repeatedly editing the generated file.
