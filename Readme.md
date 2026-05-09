<div align="center">

<br>

![banner](https://img.shields.io/badge/OBSIDIAN-RESEARCH%20VAULT-7c3aed?style=for-the-badge&labelColor=1e1b4b)

### A structured vault for deep study and content production

[![Obsidian](https://img.shields.io/badge/Obsidian-7C3AED?style=flat-square&logo=obsidian&logoColor=white)](https://obsidian.md/)&nbsp;![Template](https://img.shields.io/badge/type-vault%20template-4f46e5?style=flat-square)

<br>

</div>

---

## Purpose

This vault has two goals that must stay separated:

1. **Your own learning** — understanding the material deeply
2. **Content production** — writing articles, posts, or notes with real value for others

Mixing them creates chaos. The structure enforces the separation.

---

## Architecture

```
Resource (book / course / paper series)
  └── Part / Module  (optional grouping)
       └── Unit  (chapter / lesson / paper)
            ├── unit-learning.md   ← private thinking space
            └── unit-article.md   ← finished output for readers
```

Cross-cutting ideas that appear across multiple units live in `_concepts/`.

---

## Folder Structure

```
vault/
  _index.md              -- Dashboard: progress table for all units
  _concepts/             -- Cross-unit concept notes (emerge as you study)
  _templates/            -- Templates for learning and article files
  Attachments/           -- Images, PDFs, and other files
  part-1-<name>/         -- Optional: group units by part / module
    unit-01-<name>/
      unit-01-<name>-learning.md
      unit-01-<name>-article.md
```

Parts are optional. If your resource has no parts, put units directly at the vault root.

---

## The Two Note Types

### `unit-learning.md` — Your private thinking space

Write freely here while studying. No need to be structured — this is for you.

- Raw notes, doubts, reactions
- Questions you can't answer yet
- Connections to things you already know
- Link to `_concepts/` using `[[concept-name]]` syntax
- Status flow: `not-started` → `reading` → `done`

### `unit-article.md` — The output

Written for the reader, not for you. Start this **only after** the learning file feels complete.

- No internal links — it's a finished product, not a node in your thinking
- Linear, clean, self-contained
- Focuses on: real problem, clear explanation, examples, interactive element
- Status flow: `draft` → `review` → `published`

---

## Workflow per Unit

1. **READ** the unit with `unit-learning.md` open
   - Write raw notes, doubts, reactions
   - No structure required at this stage

2. **CONNECT** after finishing the unit
   - Review your notes
   - Identify concepts that appear in multiple units
   - Create or update `_concepts/` notes
   - Add `[[links]]` in the learning file

3. **PRODUCE** only after steps 1 and 2
   - Open `unit-article.md`
   - Use the learning file as your source, not the original material directly
   - Focus on: what's the real problem, one clear explanation, examples

---

## Concept Notes (`_concepts/`)

Cross-unit concepts that appear in more than one place in your resource.

**Do not create these upfront.** Let them emerge while studying. When you write something in a learning file and think "I'll see this again" — that's when you create the concept note and link to it.

---

## Linking Rules

**DO link in `unit-learning.md`:**
- `[[concept-name]]` to connect to `_concepts/`
- `[[unit-03-slug/unit-03-slug-learning]]` if a unit reminds you of another

**DO NOT link in `unit-article.md`:**
- The article file has no internal links
- It's a finished product, not a node in your thinking

---

## Status Tracking

Each file declares its `type` and `status` in frontmatter:

| File | Status flow |
|------|-------------|
| `unit-learning.md` | `not-started` → `reading` → `done` |
| `unit-article.md` | `draft` → `review` → `published` |

The `_index.md` dashboard reflects these statuses across all units.

---

## Graph View

Use it after completing 3+ units.

What to look for:
- Concepts connected to many units = core ideas of the resource, worth a standalone article
- Isolated learning notes = unit may need more reflection before writing

---

## Setup for a New Resource

1. Fill in `_index.md` frontmatter (`title`, `resource`, `author`)
2. Add a row to the dashboard table for each chapter / lesson
3. Create unit folders: `part-X-slug/unit-XX-slug/`
4. Apply `_templates/unit-learning` and `_templates/unit-article` to each new unit
5. Start reading — fill in the learning file first

---

<div align="center">

*Keep learning and output separated. The structure does the work.*

</div>
