---
name: nika-library
description: Use to find the user's existing work in their Nika Library (documents, images, videos, music, apps, saved work), or to save a finished deliverable there so the user keeps it in Nika.
---

# The Nika Library

- **Find:** `search_library` with a `query` and/or `type` (`document`, `art`, `video`, `music`, `product`, `Games`…), then `get_library_item` for a document's text or a file's download link.
- **Save:** `save_to_library` with:
  - `text` for documents and markdown, or
  - `content_base64` + `file_name` for a file (up to 15 MB).
- Give saved items clear names ("Q4 launch plan — Acme Bakery", not "output").
- Save finished deliverables the user will want later: plans, reports, copy, generated assets, a summary of code you wrote. Don't save scratch work.
