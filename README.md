# Poyomi's Tag Shuffler – Release 1.0

**Poyomi's Tag Shuffler** is a browser-based prompt generator designed for AI image generation.
It randomly combines tags from structured categories and subsections to produce prompts that can be used in AI art tools such as Stable Diffusion, NovelAI, or other tag-based image generators.

The goal of this tool is to make prompt creation faster, more varied, and more experimental while still allowing precise control over what kinds of tags are used.

Unlike simple random generators, the Tag Shuffler allows users to control categories, filter prompts, lock selections, group categories together, and even customize their own tag pools.

---

# Features

Release 1.0 includes the following core features.

### Tag-based prompt generation

The generator combines tags from predefined categories and subsections to create prompts automatically.

### Multiple generation modes

The generator includes several modes designed for different levels of content.

* **PG-13**
* **X**
* **XXX**
* **Custom**

Each mode controls which categories are used to generate prompts.

### Category and subsection structure

Tags are organized into categories such as:

* Hairstyles
* Clothing
* Body types
* Environments
* Camera angles
* Species

Many categories also include **subsections**, allowing more detailed control over the types of tags selected.

Example:

```
Hairstyles
 ├─ Braids
 ├─ Ponytails
 ├─ Length and volume
```

### Category grouping

Multiple categories can be grouped so that **one tag is selected from any of them**.

Example rule:

```
Hairstyles||Headwear||Accessories
```

This tells the generator to pick **one tag from any of those categories**.

### Subsection filtering

Rules can also include or exclude subsections.

Examples:

```
Hairstyles::Braids
```

Pick only from the *Braids* subsection.

```
Hairstyles::!Braids|Buns
```

Pick from Hairstyles but **exclude Braids and Buns**.

### Tag locking

Individual categories can be locked so they remain unchanged when generating new prompts.

This is useful if you want to experiment while keeping certain elements constant.

Example:

* Lock **Hair color**
* Shuffle the rest of the prompt

### Prompt history

Generated prompts are stored in a scrollable history list.
Clicking a previous prompt automatically copies it to the clipboard.

### Prompt list filtering (Blacklist / Whitelist)

Users can filter individual tags using the Prompt List panel.

This allows removing unwanted tags from generation or limiting generation to specific tags.

### Import / Export tag pools

Custom tag sets can be imported or exported using JSON files.

This makes it easy to:

* modify categories
* share tag pools
* build specialized generators

### Custom mode

Custom mode allows selecting exactly which categories should be used during generation.

Users can also control how subsections behave:

* single random subsection
* one tag per subsection

---

# Getting Started

Poyomi's Tag Shuffler runs entirely in the browser and requires no installation.

### Option 1 – Run locally

1. Download or clone the repository.

```
git clone https://github.com/Ch8f/ai-tag-prompt-shuffler-randomizer-for-image-generation.git
```

2. Open the HTML file in your browser.

```
Poyomi's Tag Shuffler - Release_1.0.html
```

The generator will run immediately.

---

### Option 2 – Use GitHub Pages (future option)

If a hosted version is provided, the generator can be used directly in a browser without downloading anything.

---

# Using the Generator

## Generation Buttons

At the top of the interface are the main generation buttons.

### PG-13

Generates prompts using categories designed to produce mostly safe content.

Note that depending on the AI model used, the output may still occasionally produce mature content.

### X

Uses additional categories that allow more mature prompts.

### XXX

Includes all categories including explicit ones.

### Custom

Allows manual control over which categories are used.

---

# Custom Mode

Custom mode opens the **Custom Selection panel**.

Here users can:

* choose which categories are used
* search for categories
* select specific subsections
* control subsection generation behavior

### Category selection

Each category has an **Include** checkbox.

When enabled, the category will be used during generation.

### Subsection controls

If a category has subsections, additional controls appear:

**Single pick**

Select one tag from a random subsection.

**One per subsection**

Generate one tag from every selected subsection.

This can dramatically increase prompt detail.

---

# Category Cards

After generating a prompt, each category appears as a card.

Each card shows:

* the selected tag
* the category name
* the number of available keywords

### Reroll button

Rerolls only that specific category.

### Lock checkbox

Locks the category so it stays the same during future generations.

---

# Prompt List (Blacklist / Whitelist)

The **Prompt List** panel allows controlling individual tags.

This is useful if:

* you dislike certain tags
* you want to avoid specific styles
* you want to limit generation to specific tags

---

## Blacklist Mode

Blacklist mode allows everything **except** selected tags.

Example:

Blacklist

```
pigtails
mohawk
buzzcut
```

These tags will never appear.

---

## Whitelist Mode

Whitelist mode allows **only** selected tags.

Example:

Whitelist

```
ponytail
braid
long hair
```

Only these tags will be used.

---

## Searching tags

The search field can find:

* category names
* subsection names
* individual tags

This makes it easier to manage large tag lists.

---

# Prompt History

Every generated prompt is stored in the History panel.

Clicking an entry copies the prompt to the clipboard.

The history automatically stores the most recent prompts for quick reuse.

---

# Importing Custom Tag Pools

Custom tag sets can be imported using the **Import JSON** button.

The JSON must contain:

```
categories
subsections
rules
```

Once imported, the generator will use the new tag pool.

---

# Exporting Tag Pools

The current tag pool can be exported using **Export JSON**.

This is useful for:

* backups
* sharing prompt setups
* modifying the tag structure externally

---

# Tips for Effective Prompt Generation

Some useful strategies when using the Tag Shuffler:

### Lock key features

Lock elements such as:

* character type
* hairstyle
* clothing

Then shuffle the rest.

### Use grouped categories

Grouping categories creates more natural prompt diversity.

Example:

```
Hairstyles||Headwear||Accessories
```

### Use subsection filtering

Exclude unwanted styles.

Example:

```
Hairstyles::!Braids
```

---

# Feedback and Future Improvements

Since this is **Release 1.0**, feedback and suggestions are very welcome.

Some potential improvements for future versions include:

### Category expansion

Additional tag categories could include:

* Lighting
* Color palettes
* Art styles
* Camera lenses
* Mood and atmosphere
* Background elements

### Weighted category selection

Allow categories to appear more often than others.

Example:

```
Hairstyles*3||Headwear
```

### Prompt templates

Allow structured prompts like:

```
(character), (clothing), (pose), (environment)
```

### Advanced conditional rules

Rules that trigger new categories based on earlier selections.

Example:

```
if species = dragon
→ include wings
```

### Preset profiles

Allow saving different prompt presets for:

* portraits
* landscapes
* character design
* fantasy scenes

### Tag popularity weighting

Some tags could appear more frequently to improve prompt quality.

---

# Contributing

If you have ideas, suggestions, or tag lists to add, feel free to open an issue or submit improvements.

Feedback is especially appreciated for:

* new tag categories
* rule system improvements
* UI enhancements
* generation logic

---

# Final Notes

Poyomi's Tag Shuffler is designed to make prompt generation both powerful and flexible while remaining simple to use.

Whether you want quick inspiration or highly controlled prompt structures, the generator can adapt to many different workflows.
