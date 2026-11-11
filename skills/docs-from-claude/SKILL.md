---
name: docs-from-claude
description: Use when the user wants to read, find, change or publish pages on their Documarium docs site, for example "update the refund policy", "where do we state the refund window", or "publish the FAQ change".
---

# Working on a Documarium docs site

The Documarium connector exposes the site's pages as tools. Work in this order:

1. **Find before you write.** Use `list_pages` and `read_page` to read the current text. When a fact is
   changing (a price, a limit, a policy date), call `find_references` first so every page that states it
   is changed together.
2. **Draft, then show.** Use `propose_edit` for each change and open the preview, so the user sees the
   page as readers will before anything goes live.
3. **Publish only on the user's word.** Call `publish` after the user approves the preview. Publishing
   needs a paid plan; if the site cannot publish yet, say so and leave the draft in place.
4. **Put it back if asked.** `history` shows what changed and who saved it; `rollback` restores an
   earlier version.

Keep the user's wording and the site's existing style. Do not invent facts, prices or legal terms; ask
the user when the source of a fact is unclear.
