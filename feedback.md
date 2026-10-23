---
name: feedback-preferences
description: Coding style and collaboration preferences observed working on HerSetsWeb
metadata:
  node_type: memory
  type: feedback
  originSessionId: 03e9b681-b6a1-45e3-bb3d-17cd34dbf05b
  modified: 2026-10-06T01:33:28.404Z
---

Keep responses short and action-focused. Iryna gives brief instructions and expects direct execution without lengthy explanation upfront.

**Why:** Observed throughout the session — she sends short messages and expects work done, not a plan narrated back at her.

**How to apply:** Do the work, give a short summary of what changed. Skip preamble.

---

Use `data-en` / `data-uk` attributes on all new user-visible text elements, and add `class="uk-namu"` for font switching.

**Why:** The site is bilingual (English + Ukrainian). Missing these breaks the language toggle.

**How to apply:** Every string added to index.html or faq.html needs both attributes. Ukrainian translations can be approximate if not provided.

---

Images in phone mockups use `object-fit: cover; object-position: top` inside `.iphone-sm-inner`.

**Why:** Screenshots are full-app captures; cropping from the top shows the most relevant content.

**How to apply:** Always use this when placing a new screenshot inside an iphone-sm wrapper.

---

Preview (data: URI) cannot load local images — they appear black. This is expected; the live GitHub Pages site renders them correctly.

**Why:** Confirmed multiple times during session. Not a bug to fix.

**How to apply:** Do not attempt to fix black images in the preview. Verify structure via `get_page_text` or JS instead.
