<div align="center">

<br>

![banner](https://img.shields.io/badge/OBSIDIAN-RESEARCH%20VAULT-7c3aed?style=for-the-badge&labelColor=1e1b4b)

### A structured knowledge base for deep technical research

[![Obsidian](https://img.shields.io/badge/Obsidian-7C3AED?style=flat-square&logo=obsidian&logoColor=white)](https://obsidian.md/)&nbsp;[![Based on kepano](https://img.shields.io/badge/based%20on-kepano--obsidian-0ea5e9?style=flat-square)](https://github.com/kepano/kepano-obsidian)&nbsp;![Template](https://img.shields.io/badge/type-vault%20template-4f46e5?style=flat-square)

<br>

</div>
 By Andrés Dalla Rizza
---

## Architecture

Everything in this vault follows one pattern:

```
Template  -->  Note  -->  Category (via Base)
```

> **The `categories` frontmatter field** connects a note to its database view.
> **The `tags` field** tracks status — driving filtered views in every Base.

1. You create a note from a **Template** (which sets the frontmatter schema)
2. The note lives in `References/` (or `Notes/`, `Clippings/`)
3. The **Category** page automatically displays it through an embedded **Base** query

---

## Folder Structure

```
research-vault/
  Categories/     -- Database views (one per category, embeds a .base file)
  References/     -- All your reference entries (papers, concepts, people, tools...)
  Notes/          -- Standalone notes, scratch work, deeper analysis
  Clippings/      -- Saved articles and blog posts from the web
  Daily/          -- Daily research log
  Templates/      -- Frontmatter templates for each note type
    Bases/        -- Database definitions (.base files)
  Attachments/    -- Images, PDFs, and other files
```

---

## Categories

### Research Core

| Category | What goes here | Status flow |
|----------|---------------|-------------|
| **Papers** | Academic papers, whitepapers, technical publications | ![to-read](https://img.shields.io/badge/-to--read-6366f1?style=flat-square) ![reading](https://img.shields.io/badge/-reading-f59e0b?style=flat-square) ![read](https://img.shields.io/badge/-read-10b981?style=flat-square) ![summarized](https://img.shields.io/badge/-summarized-059669?style=flat-square) |
| **Concepts** | Atomic knowledge units (ZK-SNARKs, transformers, Merkle trees...) | ![learning](https://img.shields.io/badge/-learning-f97316?style=flat-square) ![understood](https://img.shields.io/badge/-understood-0ea5e9?style=flat-square) ![mastered](https://img.shields.io/badge/-mastered-8b5cf6?style=flat-square) |
| **Protocols** | Technical specs and systems (Ethereum, IPFS, TLS...) | ![protocols](https://img.shields.io/badge/-protocols-64748b?style=flat-square) |
| **Indexes** | Curated maps of content per research domain | ![index](https://img.shields.io/badge/-index-4f46e5?style=flat-square) |
| **Questions** | Open research questions and hypotheses | ![open](https://img.shields.io/badge/-open-ef4444?style=flat-square) ![investigating](https://img.shields.io/badge/-investigating-f97316?style=flat-square) ![answered](https://img.shields.io/badge/-answered-10b981?style=flat-square) |

### Resources

| Category | What goes here | Status flow |
|----------|---------------|-------------|
| **Books** | Technical books | ![to-read](https://img.shields.io/badge/-to--read-6366f1?style=flat-square) ![reading](https://img.shields.io/badge/-reading-f59e0b?style=flat-square) ![read](https://img.shields.io/badge/-read-10b981?style=flat-square) |
| **Courses** | Online courses, tutorials, lecture series | ![to-take](https://img.shields.io/badge/-to--take-6366f1?style=flat-square) ![in-progress](https://img.shields.io/badge/-in--progress-f59e0b?style=flat-square) ![completed](https://img.shields.io/badge/-completed-10b981?style=flat-square) |
| **Tools** | Frameworks, libraries, dev tools | ![tools](https://img.shields.io/badge/-tools-64748b?style=flat-square) |
| **Clippings** | Saved web articles and blog posts | ![clippings](https://img.shields.io/badge/-clippings-64748b?style=flat-square) |

### Network

| Category | What goes here | Template |
|----------|---------------|----------|
| **People** | Researchers, authors, thought leaders | People Template |
| **Companies** | Labs, startups, foundations, orgs | Company Template |
| **Events** | Conferences, hackathons, workshops | Event Template |

### Personal

| Category | What goes here | Template |
|----------|---------------|----------|
| **Projects** | Your own research projects and implementations | Project Template |
| **Posts** | Your writing -- blog posts, articles, threads | Post Template |
| **Evergreen** | Distilled insights in your own words | Evergreen Template |
| **Journal** | Free-form research journal entries | Journal Template |
| **Meetings** | Study groups, research meetings | Meeting Template |
| **Daily Notes** | Daily research log | Daily Note Template |

---

## How to Use

### 1. Starting a new research domain

Create an **Index** note. This is your map of content for a topic area.

1. <kbd>Ctrl</kbd>+<kbd>N</kbd> to create a new note
2. Apply the **Index Template** (<kbd>Ctrl</kbd>+<kbd>T</kbd> or via the command palette)
3. Name it after the domain: "Zero Knowledge Proofs", "Large Language Models", etc.
4. Fill in the sections over time as you learn -- link to concepts, papers, tools, and people

> An Index is not a database. It is your hand-written guide to a topic. You decide the structure, the ordering, and the narrative. The Category pages handle the database views automatically.

### 2. Adding a paper

1. Create a new note, apply the **Paper Template**
2. Fill in the frontmatter: `author`, `year`, `venue`, `field`, `doi`, `url`
3. Set the tag to ![to-read](https://img.shields.io/badge/-to--read-6366f1?style=flat-square)
4. Write your notes as you read -- use the Abstract, Key Contribution, Methodology, Results, and Notes sections
5. When done, change the tag to ![read](https://img.shields.io/badge/-read-10b981?style=flat-square) or ![summarized](https://img.shields.io/badge/-summarized-059669?style=flat-square)
6. The paper automatically appears in the Papers category under the right views

### 3. Breaking down concepts

When you encounter an important idea inside a paper, book, or course:

1. Create a **Concept** note for it
2. Fill in `field`, `difficulty`, `prerequisites`, and `related-concepts`
3. Write it in your own words -- the Definition, Intuition, and How It Works sections
4. Link back to the source and forward to related concepts
5. Change the tag from ![learning](https://img.shields.io/badge/-learning-f97316?style=flat-square) to ![understood](https://img.shields.io/badge/-understood-0ea5e9?style=flat-square) when you can explain it without looking

### 4. Tracking questions

When something confuses you or you identify a gap in your understanding:

1. Create a **Question** note
2. Tag it ![open](https://img.shields.io/badge/-open-ef4444?style=flat-square)
3. As you investigate, add findings to the Investigation section and change the tag to ![investigating](https://img.shields.io/badge/-investigating-f97316?style=flat-square)
4. When resolved, fill in the Answer section, link to the `answer-note`, and tag it ![answered](https://img.shields.io/badge/-answered-10b981?style=flat-square)

### 5. Connecting everything

The power of this vault comes from **links between notes**:

- A Paper links to its Authors (People), the Concepts it introduces, and the Protocol it describes
- A Concept links to its Prerequisites (other Concepts), the Papers that define it, and the Tools that implement it
- An Index links to everything relevant in a domain, organized by your understanding
- A Question links to the Concepts it relates to and the Paper or note that answered it

Use `[[double brackets]]` liberally. The graph view (<kbd>Ctrl</kbd>+<kbd>G</kbd>) will show you the structure of your knowledge.

### 6. Daily research log

Use **Daily Notes** (<kbd>Ctrl</kbd>+<kbd>D</kbd> or click the calendar icon) to log what you worked on each day. The Daily.base embedded in each daily note shows related entries. Use Journal entries for longer-form thinking.

### 7. Evergreen notes

When you understand something deeply enough to express it as a standalone insight:

1. Create an **Evergreen** note
2. Write a single, clear idea -- something composable that can be linked from many places
3. These are the refined output of your research process

---

## Workflow Summary

```
Discover  ──────────────────────────────────────────────────  Distill

  Paper       ──►  to-read      ──►  reading      ──►  Link        ──►  Evergreen
  Course      ──►  to-take      ──►  in-progress       Concepts,        note
  Clipping    ──►  clippings    ──►  Notes              People,
  Book        ──►  to-read      ──►  Concepts           Protocols
  Question    ──►  open         ──►  investigating ──►  answered
```

---

## Status Tags Reference

Tags drive the filtered views in each Base. Change them to move notes through your pipeline.

| Tag | Used in | Meaning |
|-----|---------|---------|
| ![to-read](https://img.shields.io/badge/-to--read-6366f1?style=flat-square) | Papers, Books | Queued for reading |
| ![reading](https://img.shields.io/badge/-reading-f59e0b?style=flat-square) | Papers, Books | Currently reading |
| ![read](https://img.shields.io/badge/-read-10b981?style=flat-square) | Papers, Books | Finished reading |
| ![summarized](https://img.shields.io/badge/-summarized-059669?style=flat-square) | Papers | Read and summarized with notes |
| ![learning](https://img.shields.io/badge/-learning-f97316?style=flat-square) | Concepts | Currently learning this concept |
| ![understood](https://img.shields.io/badge/-understood-0ea5e9?style=flat-square) | Concepts | Can explain it in your own words |
| ![mastered](https://img.shields.io/badge/-mastered-8b5cf6?style=flat-square) | Concepts | Deep understanding, can teach it |
| ![to-take](https://img.shields.io/badge/-to--take-6366f1?style=flat-square) | Courses | Queued for taking |
| ![in-progress](https://img.shields.io/badge/-in--progress-f59e0b?style=flat-square) | Courses | Currently taking |
| ![completed](https://img.shields.io/badge/-completed-10b981?style=flat-square) | Courses | Finished the course |
| ![open](https://img.shields.io/badge/-open-ef4444?style=flat-square) | Questions | Unanswered question |
| ![investigating](https://img.shields.io/badge/-investigating-f97316?style=flat-square) | Questions | Actively looking for an answer |
| ![answered](https://img.shields.io/badge/-answered-10b981?style=flat-square) | Questions | Resolved with an answer |
| ![index](https://img.shields.io/badge/-index-4f46e5?style=flat-square) | Indexes | Map of content note |
| ![0pine](https://img.shields.io/badge/-0pine-34d399?style=flat-square) | Evergreen | Distilled insight (the pine tree icon) |
| ![daily](https://img.shields.io/badge/-daily-64748b?style=flat-square) | Daily Notes | Daily log entry |

---

## Obsidian Features Enabled

| Feature | What it does |
|---------|-------------|
| **Bases** | Database views embedded in category pages -- the core of the vault's organization |
| **Properties** | Visual editor for frontmatter in the sidebar -- makes editing metadata fast |
| **Outgoing Links** | Shows what a note links to -- essential for seeing connections |
| **Backlinks** | Shows what links to a note -- discover unexpected connections |
| **Graph View** | Visual map of your entire knowledge graph |
| **Canvas** | Freeform visual boards -- use for mapping relationships between concepts |
| **Word Count** | Status bar word count -- helpful for writing |
| **Footnotes** | Insert footnotes for academic-style citations |
| **Templates** | Apply frontmatter schemas to new notes with one command |
| **Daily Notes** | One-click daily research log creation |
| **Zettelkasten Prefixer** | Unique ID generation for notes (YYYY-MM-DD HHmm format) |
| **Bookmarks** | Pin frequently accessed notes and searches |
| **Outline** | Table of contents for the current note |
| **Tags** | Tag-based filtering and navigation |

---

<details>
<summary><strong>Tips</strong></summary>
<br>

- **Name notes clearly.** "zk-SNARKs" not "ZK stuff". Good names make linking natural.
- **Link aggressively.** Every time you mention a concept, person, or paper that exists in your vault, link it with `[[brackets]]`. Links are the structure.
- **Use the graph view** (<kbd>Ctrl</kbd>+<kbd>G</kbd>) to spot clusters and orphan notes. Orphans need more connections.
- **Indexes are your home pages.** When you sit down to study a topic, start from its Index.
- **Let questions drive research.** Create a Question note before searching for the answer. It keeps you focused.
- **Evergreen notes are the output.** Papers, courses, and clippings are inputs. Evergreen notes are what you actually learned, in your own words.
- **Update status tags.** Moving a paper from `to-read` to `read` is how the base views stay useful.
- **Use Canvas for visual mapping.** Drag notes onto a canvas to see how concepts in a domain relate visually.
- **Daily notes build momentum.** Even a one-line entry per day creates a log you can look back on.

</details>

---

## Get Started

1. Open this vault in Obsidian
2. Create your first **Index** for a topic you want to research (e.g., "Zero Knowledge Proofs")
3. Start adding **Papers**, **Concepts**, and **Tools** as you find them
4. Link everything together
5. Distill your understanding into **Evergreen** notes

---

<div align="center">

*Built on the [kepano vault template](https://github.com/kepano/kepano-obsidian). Restructured for technical research.*

</div>
