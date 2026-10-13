---
name: Patch hunk context
description: Avoid rejected or partial file edits when applying several replacements.
---

When editing several separate areas of a file, start a new patch hunk for each area and copy the current complete line as context. Earlier edits can make a later hunk's original context stale; a failed patch is atomic and changes nothing.

**Why:** Applying multiple updates against outdated or discontinuous context caused rejected edits and wasted implementation time.

**How to apply:** Read or grep the current target immediately before patching, group only adjacent replacements together, and verify the diff afterward.
