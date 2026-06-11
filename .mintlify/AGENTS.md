# Agent instructions — my-app documentation

## Source-to-docs mapping
- The source repo `my-app` is documented by the pages in this repo.
- `src/auth.py` (authentication policy) is documented by `docs/authentication.mdx`.
  When that file changes, update that page.

## Hard rules
- Update **existing pages only**. Never create new pages, rename, or delete pages.
- Keep each page's YAML frontmatter intact, with a `title` as the first field.
- Preserve the existing headings, table structure, and tone of the page.

## Accuracy rules (the point of this doc)
- The page must state the **exact values** from the code. Specifically, mirror
  these constants from `src/auth.py` into `docs/authentication.mdx`:
  - `MAX_FAILED_ATTEMPTS`  → the "Account lockout" number
  - `MIN_PASSWORD_LENGTH`  → the "Minimum password length" number
  - `SESSION_TIMEOUT_MINUTES` → the "Session timeout" number
- Mirror the `reason` strings returned by `login()` into the "Responses" table.
- If a constant or a `reason` value changes in the code, change the matching
  number/string on the page so it always reflects the code exactly.

## Style
- Plain, factual product documentation. Short sentences. State concrete numbers.
