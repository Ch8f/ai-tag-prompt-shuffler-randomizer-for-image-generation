# Poyomi’s Tag Shuffler – Release 1.0

Hi!
Welcome to **Poyomi’s Tag Shuffler**.

This is a browser-based prompt generator I built to help create prompts for AI image generation tools like **Stable Diffusion, NovelAI, and other tag-based generators**.

The idea is simple:
Instead of manually writing long prompts, the shuffler combines tags from structured categories to create new prompt combinations instantly.

The current configuration already contains **several thousand tags** organized across many categories and subsections, giving the generator a huge number of possible combinations.

Because of this, even after many generations you will still see a lot of variety.

---

# Why I made this

Originally, this tool was something I created **just for myself**.

I often found myself repeatedly writing prompts or trying to come up with new combinations of tags, and I thought it would be useful to have something that could automatically shuffle tags while still allowing control over what gets generated.

After working on it for a while, I realized the tool had grown into something that might be useful to other people as well.
So I decided to clean it up and release it publicly.

That said, this is still **version 1.0**, and it might not be perfect yet.
If you have ideas, suggestions, or improvements, I’m always open to feedback.

---

# What the Tag Shuffler does

Poyomi’s Tag Shuffler randomly generates prompts by combining tags from different categories.

For example, it might combine things like:

* character features
* hairstyles
* clothing
* poses
* environments
* camera angles
* art styles

All of these are organized into categories so the generator knows how to build a prompt.

The result is a prompt that can immediately be used in an AI image generator.

---

# Generation Modes

At the top of the interface you will see four main buttons.

These determine which categories are used when generating prompts.

### PG-13

This mode generates prompts using mostly safe categories.

However, depending on the AI generator you use, the resulting images **may still occasionally produce X-rated results**, even if the prompt itself appears safe.

### X

This mode allows more mature content categories.

### XXX

This mode includes all available categories, including explicit ones.

### Custom

Custom mode lets you manually choose exactly which categories should be used.

This is the most flexible option if you want to experiment with specific prompt structures.

---

# Generating Prompts

To generate a prompt, simply click one of the generation buttons.

The generator will combine tags from the selected categories and display the result in the **Generated Prompt** panel.

Each time you generate a prompt, the tool will randomly select new tags.

---

# Category Cards

After generating a prompt, you will see a list of category cards.

Each card represents one category that contributed to the prompt.

The card shows:

* the category name
* the selected tag
* how many keywords exist in that category

Each card also includes two controls.

### Reroll

This button rerolls only that specific category.

This is useful if you like most of the prompt but want to change just one part.

### Lock

Locking a category prevents it from changing during future generations.

For example, you might lock:

* a hairstyle
* a character type
* a clothing item

Then shuffle the rest of the prompt.

---

# Prompt History

Every prompt you generate is saved in the **History panel**.

This lets you easily go back to earlier prompts.

Clicking a prompt in the history will copy it to your clipboard.

---

# Custom Mode

Custom mode allows you to choose exactly which categories should be used.

When you open Custom mode, a panel appears that shows all available categories.

You can:

* include or exclude categories
* search for categories
* choose specific subsections

If a category has subsections, you can also choose how tags are generated.

### Single pick

Select one random tag from one subsection.

### One per subsection

Generate one tag from every selected subsection.

This option can produce much more detailed prompts.

---

# Prompt List (Blacklist / Whitelist)

The **Prompt List** panel gives you control over individual tags.

If there are tags you don’t want appearing in prompts, you can blacklist them.

If you want to restrict the generator to only certain tags, you can use whitelist mode.

---

## Blacklist Mode

Blacklist mode allows everything **except** the tags you select.

Example:

You might blacklist tags like:

* certain hairstyles
* specific clothing types
* styles you dislike

These tags will never appear in generated prompts.

---

## Whitelist Mode

Whitelist mode does the opposite.

Only the tags you select will be allowed.

Everything else will be ignored.

This is useful if you want to experiment with a very specific style or theme.

---

# Searching Tags

The prompt list includes a search field.

You can search for:

* category names
* subsection names
* individual tags

This makes it much easier to manage large tag lists.

---

# Importing and Exporting Tag Pools

You can also import or export the entire tag database as JSON.

This allows you to:

* customize your own tag pools
* share tag collections
* back up your configuration
* experiment with different prompt structures

---

# Tag System and Rules

The generator supports flexible rule formats for categories and subsections.

Examples include:

```
"Category"
```

Pick one tag from the entire category.

```
"Category::Subsection"
```

Pick one tag only from that subsection.

```
"Category::!Subsection"
```

Pick one tag from the category but exclude that subsection.

```
"Category||Category"
```

Pick one tag from any of the listed categories.

These rules make it possible to build very flexible prompt structures.

---

# Tag Count

The current configuration already includes **several thousand tags** across many categories and subsections.

This large tag pool allows the generator to produce an enormous number of possible prompt combinations.

Even with frequent use, the generator will continue to create new variations.

---

# Tips for Using the Shuffler

Here are a few useful ways to use the tool.

### Lock key elements

Lock the parts of the prompt you like, then reroll the rest.

### Use category groups

Grouping categories can create more varied prompts.

### Experiment with custom mode

Custom mode allows you to create very specific prompt styles.

---

# Future Improvements

Since this project is still new, there are many things that could be improved or expanded.

Possible future additions might include:

* more categories
* additional tags
* weighted tag selection
* improved UI features
* better prompt structuring
* preset generation profiles

If you have ideas or suggestions, feel free to share them.

---

# Feedback and Suggestions

Since this project started as a personal tool, I’m very interested in hearing how other people use it.

If you have ideas for:

* new tag categories
* additional tags
* feature improvements
* UI changes

please feel free to suggest them.

---

# Final Notes

Poyomi’s Tag Shuffler is meant to be a flexible tool for generating prompts quickly while still giving users a lot of control over how those prompts are created.

I hope it helps make prompt creation easier, faster, and maybe even a bit more fun.

Thanks for trying it out!
