# Note Management Strategy for This Vault

## Overview

This vault uses a **hybrid PARA + Zettelkasten system** that combines action-oriented organization (PARA) with knowledge-building (Zettelkasten).

## Folder Structure

```
garden/
├── 00-Inbox/              # Quick capture, unsorted notes
├── 10-Projects/           # Active, time-bound projects
├── 20-Areas/              # Ongoing responsibilities
├── 30-Resources/          # Reference materials, learning
├── 40-Archive/            # Completed/inactive items
├── 50-Zettelkasten/       # Permanent, atomic notes
├── 90-Templates/          # Note templates
└── 99-Meta/              # Vault maintenance, indexes
```

---

## The Two Systems

### PARA Method - The Execution Engine

Organizes information by **actionability** - how you're using it right now.

#### 00-Inbox - Your Capture Zone
- **Purpose**: Temporary holding area for all new notes
- **What goes here**: Quick thoughts, meeting notes, ideas, web clippings, anything captured quickly
- **Workflow**: Don't organize on capture - just get it down. Process weekly.
- **Processing**: Review regularly and move items to their proper homes

#### 10-Projects - Active Work (Finite Goals)
- **Purpose**: Short-term efforts with clear goals and deadlines
- **Examples**:
  - "Launch personal website"
  - "Learn Python basics"
  - "Plan summer vacation"
  - "Write research paper"
- **Key characteristic**: Has a clear end date and success criteria
- **When complete**: Move to 40-Archive
- **Structure**: Create subfolders for each project

#### 20-Areas - Ongoing Responsibilities (Infinite)
- **Purpose**: Long-term areas of life you're maintaining
- **Examples**:
  - "Health & Fitness"
  - "Career Development"
  - "Personal Finance"
  - "Home Maintenance"
  - "Relationships"
- **Key characteristic**: No end date - these continue indefinitely
- **Think**: Standards to maintain, not goals to complete
- **Structure**: One subfolder per area of responsibility

#### 30-Resources - Reference Library
- **Purpose**: Topics of interest and reference materials
- **Examples**:
  - "Cooking Recipes"
  - "Book Notes"
  - "Programming Guides"
  - "Travel Ideas"
  - "Productivity Techniques"
- **Key characteristic**: Things you might use someday, pure reference
- **When to use**: Not actively working on it, but want to keep for later

#### 40-Archive - The Attic
- **Purpose**: Inactive but kept for historical reference
- **What goes here**:
  - Completed projects
  - Inactive areas you're no longer maintaining
  - Old resources you don't need anymore
- **Don't delete**: Keep for context and history
- **Review**: Annually clean out if truly unnecessary

---

### Zettelkasten Method - The Thinking Engine

Lives in **50-Zettelkasten** - works completely differently from PARA.

#### Purpose
Build a permanent network of interconnected ideas that grows smarter over time.

#### Key Principles

**1. Atomic Notes - One Idea Per Note**
- ❌ Not: "Everything about Marketing"
- ✅ Instead: "Social proof increases conversion rates"
- Keep notes small, focused, and reusable
- Easier to link and recombine in new ways

**2. Evergreen Content - Timeless Insights**
- ❌ Not: "Meeting notes from Jan 5, 2025"
- ✅ Instead: "Effective meetings need clear agendas"
- Knowledge that doesn't expire or go stale
- Written as permanent insights, not temporary captures

**3. Written in Your Own Words**
- Don't copy-paste - paraphrase and internalize
- Forces you to truly understand the concept
- Makes ideas yours, not someone else's
- Easier to remember and apply

**4. Heavily Linked - Ideas Connect to Ideas**
- Each note links to related notes using `[[double brackets]]`
- Creates a web of knowledge, not isolated islands
- Sparks new insights through unexpected connections
- Use backlinks to see what references each note

#### When to Create a Zettelkasten Note

Ask yourself: "Is this a timeless insight I want to remember forever?"
- ✅ "Compound interest works in knowledge too"
- ✅ "Writing forces clarity of thought"
- ✅ "Small consistent habits beat motivation"
- ❌ "Grocery list for party"
- ❌ "TODO: Call dentist"
- ❌ "Notes from team meeting"

#### Naming Zettelkasten Notes

Option 1: **Descriptive titles** (recommended for beginners)
- "Social proof increases conversion.md"
- "Writing clarifies thinking.md"
- "Constraints boost creativity.md"

Option 2: **Timestamp IDs** (traditional Zettelkasten)
- "202512031045 - Social proof increases conversion.md"
- Prevents naming conflicts
- Shows chronological order

Choose one approach and stick with it.

---

## How PARA and Zettelkasten Work Together

### Think of Them as Two Different Brains

**PARA (Left Brain)** - Practical, Organized, Action-Oriented
- Answers: "What am I working on RIGHT NOW?"
- Contains: Project deadlines, task lists, active work
- Nature: Temporary - things move in and out
- Flow: Inbox → Projects/Areas/Resources → Archive

**Zettelkasten (Right Brain)** - Creative, Networked, Insight-Oriented
- Answers: "What do I understand about the world?"
- Contains: Ideas, concepts, lessons learned
- Nature: Permanent - builds up over time
- Flow: Insights extracted from anywhere → Zettelkasten forever

### Example Workflow: Learning About Productivity

**1. Capture** (00-Inbox)
- Read article about Pomodoro Technique
- Quick note: "Pomodoro article notes.md"

**2. Process into PARA**
- Currently trying to improve focus → Move to **10-Projects/Improve Focus/**
- Create actionable project note with specific tasks
- Add deadlines and next actions

**3. Extract Insights** (50-Zettelkasten)
- Create atomic note: "Time constraints increase focus.md"
- Write the concept in your own words
- Link to related notes: `[[Parkinson's Law]]`, `[[Deep Work principles]]`, `[[Flow state triggers]]`
- These insights outlive the project

**4. Reference Material** (30-Resources)
- Create "Productivity Techniques.md" with technique overview
- Link to your Zettelkasten notes for deeper understanding
- Store the original article for later reference

**5. Complete Project**
- Project finished → Move to **40-Archive/Improve Focus/**
- Zettelkasten notes stay forever in **50-Zettelkasten**
- You can reference those insights in future projects

### The Key Difference

**PARA asks**: "Where does this help me RIGHT NOW?"
- Project note: "Launch blog - tasks and deadlines"
- Lives in 10-Projects
- Gets archived when done
- Temporary and actionable

**Zettelkasten asks**: "What can I LEARN from this forever?"
- Atomic note: "Publishing consistently builds audience trust"
- Lives in 50-Zettelkasten
- Stays forever, gets richer with more links
- Permanent and conceptual

### Linking Between Systems

You can (and should) link freely between PARA and Zettelkasten:

**From Project Note:**
```markdown
# Launch Blog Project

## Key Principles to Apply
- [[Writing clarifies thinking]]
- [[Publishing consistently builds trust]]
- [[Done is better than perfect]]

## Tasks
- [ ] Set up hosting
- [ ] Design layout
```

**From Zettelkasten Note:**
```markdown
# Publishing consistently builds trust

Regular publishing creates reliability...

## Where I'm applying this
- [[10-Projects/Launch Blog]]
- [[20-Areas/Career Development]]
```

The link goes both ways, but the note stays in its proper home.

---

## Supporting Folders

### 90-Templates - Reusable Structures

Create templates for common note types:
- Daily note template
- Project template
- Meeting notes template
- Zettelkasten note template
- Book notes template

Use Obsidian's template plugin or manually copy.

### 99-Meta - Vault Housekeeping

- **This file** - System documentation
- Index notes (Maps of Content)
- Changelog of vault organization
- How-to guides for your personal workflow

---

## Weekly Review Process

Set aside 30-60 minutes weekly:

### 1. Clear Inbox (00-Inbox)
- Process ALL notes
- Move to appropriate PARA folder or Zettelkasten
- Extract insights into atomic notes
- Delete what's no longer relevant

### 2. Update Projects (10-Projects)
- Review each active project
- Update task lists and next actions
- Move completed projects to Archive
- Archive stalled projects

### 3. Maintain Areas (20-Areas)
- Review ongoing areas of responsibility
- Ensure notes are current
- Add new thoughts or updates
- Check if any areas should be archived

### 4. Enrich Zettelkasten (50-Zettelkasten)
- Review recent notes
- Add missing links between related concepts
- Combine similar notes if too granular
- Split notes if they contain multiple ideas
- Strengthen weak notes with more context

### 5. Clean Up
- Fix broken links
- Delete true duplicates
- Merge redundant notes
- Update outdated information

---

## Best Practices

### Do's ✅
- **Capture quickly** - Don't organize while capturing ideas
- **Process regularly** - Weekly inbox review minimum
- **Write in your words** - Understanding beats copying
- **Link liberally** - More connections = more insights
- **Keep notes atomic** - One clear idea per note
- **Use tags sparingly** - Structure with folders and links primarily
- **Review periodically** - System needs maintenance

### Don'ts ❌
- **Don't over-organize** - Perfect organization prevents action
- **Don't hoard** - Archive or delete what you won't use
- **Don't copy-paste blindly** - Rephrase to internalize
- **Don't create too many folders** - Keep structure simple
- **Don't skip the inbox** - It prevents overwhelm later
- **Don't orphan notes** - Link new notes to existing ones
- **Don't over-tag** - Tags without structure create chaos

---

## Decision Framework: Where Does This Note Go?

Ask these questions in order:

### 1. Is it processed yet?
- **No** → 00-Inbox (process later)

### 2. Is it a timeless insight or concept?
- **Yes** → 50-Zettelkasten (permanent knowledge)

### 3. Is it related to a specific project with a deadline?
- **Yes** → 10-Projects (active work)

### 4. Is it an ongoing area of life I'm maintaining?
- **Yes** → 20-Areas (responsibilities)

### 5. Is it reference material for potential future use?
- **Yes** → 30-Resources (reference library)

### 6. Is it completed or inactive?
- **Yes** → 40-Archive (done/inactive)

When in doubt, put it in **00-Inbox** and decide during your weekly review.

---

## Growing Your System

### Start Simple
- Begin with just the Inbox and PARA folders
- Add Zettelkasten notes gradually as you extract insights
- Don't try to retroactively organize everything at once

### Let It Evolve
- Your system will develop its own character
- Create subfolders in PARA as needed
- Develop personal conventions and shortcuts
- Trust the process - it gets easier with practice

### Measure Success By
- Can you find notes quickly?
- Do you actually use your notes?
- Are you discovering unexpected connections?
- Does the system feel helpful, not burdensome?

If yes to these, your system is working.

---

## Quick Reference

| Folder | Time Horizon | Question | Example |
|--------|--------------|----------|---------|
| 00-Inbox | Temporary | What just came in? | Random thoughts, quick captures |
| 10-Projects | Weeks-Months | What am I working on? | Launch website, Learn Python |
| 20-Areas | Years | What am I maintaining? | Health, Career, Finances |
| 30-Resources | Indefinite | What might I need? | Recipes, Book notes, Guides |
| 40-Archive | Past | What's completed? | Old projects, inactive areas |
| 50-Zettelkasten | Forever | What do I understand? | Core insights, timeless ideas |
| 90-Templates | Tool | What structure do I reuse? | Daily note, Project template |
| 99-Meta | Utility | How does my system work? | This file, indexes, guides |

---

## Further Learning

- **PARA Method**: Tiago Forte's "Building a Second Brain"
- **Zettelkasten**: "How to Take Smart Notes" by Sönke Ahrens
- **Obsidian Forums**: forum.obsidian.md
- **Practice**: The best way to learn is by doing

---

*Last updated: 2025-12-03*
*This is a living document - update as your system evolves*
