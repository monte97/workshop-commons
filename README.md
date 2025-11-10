# workshop-commons

This directory contains reusable assets for building workshop presentations with Slidev.

## Resources

### Themes

- **modern-minimal**: A modern, minimal, and professional dark theme.

### Slide Templates

- **intro/montelli-intro.md**: A standard workshop introduction slide for Francesco Montelli.

## How to Use

To use these assets in your Slidev presentation, reference them using relative paths from your main markdown file.

### Using the Theme

In the frontmatter of your `slides.md` or similar entry file, set the `theme` property.

**Example (from project root):**
```yaml
---
theme: './workshop-commons/themes/modern-minimal'
---
```

**Example (from a `slides` subdirectory):**
```yaml
---
theme: '../workshop-commons/themes/modern-minimal'
---
```

### Using Slide Templates

You can include slide templates using the `src` property on a slide separator.

**Example (from project root):**
```markdown
---
src: ./workshop-commons/slides/intro/montelli-intro.md
---
```
