# Obsidian research vault template

A research vault for [Obsidian](https://obsidian.md/) built for deep exploration of complex technical topics.

Based on the [kepano vault template](https://github.com/kepano/kepano-obsidian), restructured from a personal life-tracking system into a technical research knowledge base.

---

## Architecture

Everything in this vault follows one pattern:

```
Template  -->  Note  -->  Category (via Base)
```

1. You create a note from a **Template** (which sets the frontmatter schema)
2. The note lives in `References/` (or `Notes/`, `Clippings/`)
3. The **Category** page automatically displays it through an embedded **Base** query

The `categories` field in frontmatter is what connects a note to its database view. The `tags` field tracks status (e.g., `to-read`, `learning`, `open`).

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

| Category | What goes here | Template | Status tags |
|----------|---------------|----------|-------------|
| **Papers** | Academic papers, whitepapers, technical publications | Paper Template | `to-read` / `reading` / `read` / `summarized` |
| **Concepts** | Atomic knowledge units (ZK-SNARKs, transformers, Merkle trees...) | Concept Template | `learning` / `understood` / `mastered` |
| **Protocols** | Technical specs and systems (Ethereum, IPFS, TLS...) | Protocol Template | `protocols` |
| **Indexes** | Curated maps of content per research domain | Index Template | `index` |
| **Questions** | Open research questions and hypotheses | Question Template | `open` / `investigating` / `answered` |

### Resources

| Category | What goes here | Template | Status tags |
|----------|---------------|----------|-------------|
| **Books** | Technical books | Book Template | `to-read` / `reading` / `read` |
| **Courses** | Online courses, tutorials, lecture series | Course Template | `to-take` / `in-progress` / `completed` |
| **Tools** | Frameworks, libraries, dev tools | Tool Template | `tools` |
| **Clippings** | Saved web articles and blog posts | Clipping Template | `clippings` |

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

1. `Ctrl+N` to create a new note
2. Apply the **Index Template** (`Ctrl+T` or via the command palette)
3. Name it after the domain: "Zero Knowledge Proofs", "Large Language Models", etc.
4. Fill in the sections over time as you learn -- link to concepts, papers, tools, and people

An Index is not a database. It is your hand-written guide to a topic. You decide the structure, the ordering, and the narrative. The Category pages handle the database views automatically.

### 2. Adding a paper

1. Create a new note, apply the **Paper Template**
2. Fill in the frontmatter: `author`, `year`, `venue`, `field`, `doi`, `url`
3. Set the tag to `to-read`
4. Write your notes as you read -- use the Abstract, Key Contribution, Methodology, Results, and Notes sections
5. When done, change the tag from `to-read` to `read` or `summarized`
6. The paper automatically appears in the Papers category under the right views

### 3. Breaking down concepts

When you encounter an important idea inside a paper, book, or course:

1. Create a **Concept** note for it
2. Fill in `field`, `difficulty`, `prerequisites`, and `related-concepts`
3. Write it in your own words -- the Definition, Intuition, and How It Works sections
4. Link back to the source and forward to related concepts
5. Change the tag from `learning` to `understood` when you can explain it without looking

### 4. Tracking questions

When something confuses you or you identify a gap in your understanding:

1. Create a **Question** note
2. Tag it `open`
3. As you investigate, add findings to the Investigation section and change the tag to `investigating`
4. When resolved, fill in the Answer section, link to the `answer-note`, and tag it `answered`

### 5. Connecting everything

The power of this vault comes from **links between notes**:

- A Paper links to its Authors (People), the Concepts it introduces, and the Protocol it describes
- A Concept links to its Prerequisites (other Concepts), the Papers that define it, and the Tools that implement it
- An Index links to everything relevant in a domain, organized by your understanding
- A Question links to the Concepts it relates to and the Paper or note that answered it

Use `[[double brackets]]` liberally. The graph view (`Ctrl+G`) will show you the structure of your knowledge.

### 6. Daily research log

Use **Daily Notes** (`Ctrl+D` or click the calendar icon) to log what you worked on each day. The Daily.base embedded in each daily note shows related entries. Use Journal entries for longer-form thinking.

### 7. Evergreen notes

When you understand something deeply enough to express it as a standalone insight:

1. Create an **Evergreen** note
2. Write a single, clear idea -- something composable that can be linked from many places
3. These are the refined output of your research process

---

## Workflow Summary

```
Discover  -->  Capture  -->  Process  -->  Connect  -->  Distill

 Paper        to-read       reading        Link to         Evergreen
 Course       to-take       in-progress    Concepts,       note
 Clipping     clippings     Notes          People,
 Book         to-read       Concepts       Protocols
 Question     open          investigating  answered
```

---

## Status Tags Reference

Tags drive the filtered views in each Base. Change them to move notes through your pipeline.

| Tag | Used in | Meaning |
|-----|---------|---------|
| `to-read` | Papers, Books | Queued for reading |
| `reading` | Papers, Books | Currently reading |
| `read` | Papers, Books | Finished reading |
| `summarized` | Papers | Read and summarized with notes |
| `learning` | Concepts | Currently learning this concept |
| `understood` | Concepts | Can explain it in your own words |
| `mastered` | Concepts | Deep understanding, can teach it |
| `to-take` | Courses | Queued for taking |
| `in-progress` | Courses | Currently taking |
| `completed` | Courses | Finished the course |
| `open` | Questions | Unanswered question |
| `investigating` | Questions | Actively looking for an answer |
| `answered` | Questions | Resolved with an answer |
| `index` | Indexes | Map of content note |
| `0pine` | Evergreen | Distilled insight (the pine tree icon) |
| `daily` | Daily Notes | Daily log entry |

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

## Tips

- **Name notes clearly.** "zk-SNARKs" not "ZK stuff". Good names make linking natural.
- **Link aggressively.** Every time you mention a concept, person, or paper that exists in your vault, link it with `[[brackets]]`. Links are the structure.
- **Use the graph view** (`Ctrl+G`) to spot clusters and orphan notes. Orphans need more connections.
- **Indexes are your home pages.** When you sit down to study a topic, start from its Index.
- **Let questions drive research.** Create a Question note before searching for the answer. It keeps you focused.
- **Evergreen notes are the output.** Papers, courses, and clippings are inputs. Evergreen notes are what you actually learned, in your own words.
- **Update status tags.** Moving a paper from `to-read` to `read` is how the base views stay useful.
- **Use Canvas for visual mapping.** Drag notes onto a canvas to see how concepts in a domain relate visually.
- **Daily notes build momentum.** Even a one-line entry per day creates a log you can look back on.

---

## Get Started

1. Open this vault in Obsidian
2. Create your first **Index** for a topic you want to research (e.g., "Zero Knowledge Proofs")
3. Start adding **Papers**, **Concepts**, and **Tools** as you find them
4. Link everything together
5. Distill your understanding into **Evergreen** notes

---

*Built on the [kepano vault template](https://github.com/kepano/kepano-obsidian). Restructured for technical research.*
