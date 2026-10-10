---
layout: page
title: Github Pages
permalink: /subjects/github-pages

---

# Github Pages

## Steps to Create a Notes Site using Markdown Only

1. Create a new repository
2. Create a file named "_config.yml" -- This file is to write the Jekyll configurations in
   Add this in the "_config.yml" file.
   ```
   title: My Notes
   description: My personal notes and knowledge base
   theme: minima
   markdown: kramdown
   ```
   What this does:
     - title sets your site's name.
     - description describes your site.
     - theme: minima tells Jekyll to use the Minima theme, which GitHub Pages supports.
     - markdown: kramdown selects the Markdown processor
3. Create your homepage. Which is just a file named "index.md"
   Add this in the "index.md" file.
  
   ```
     ---
     layout: home
     title: Home
     ---
     
     # Welcome to My Notes
     
     This is my personal knowledge base.
     
     I organize my notes by subject, topic, and subtopic.
     
     ## Browse Subjects
     
     - [Mathematics](subjects/mathematics/)
     - [Computer Science](subjects/computer-science/)
     - [Physics](subjects/physics/)
     
     I'll keep adding notes as I learn new things.
   ```
   The section between the first pair of --- markers is called front matter. It provides information to Jekyll about the page. The rest is your Markdown content.
   The layout: home setting uses the homepage layout provided by Minima. Later, you can replace it with your own card-based layout.

# Creating Pages in Jekyll with Markdown

## 1. What is Front Matter?

Front matter is a block of YAML metadata at the very beginning of a Markdown file. Jekyll uses it to identify and configure a page.

It must be enclosed between two lines containing three hyphens (`---`).

Example:

```yaml
---
layout: page
title: Derivatives
permalink: /subjects/mathematics/calculus/derivatives/
---
```

### Common Front Matter Fields

- `layout`: The HTML template used to display the page.
- `title`: The page title.
- `permalink`: The URL where the page will appear.
- `description`: A short description of the page.
- `parent`: The parent page's title in themes that support hierarchical navigation, such as Just the Docs.
- `nav_order`: Controls the page's position in supported navigation menus.

You don't need every field on every page. Use the fields appropriate for your theme and configuration.

## 2. Creating a Page

Create a Markdown file in the appropriate folder in your GitHub repository.

Example path:

`subjects/mathematics/calculus/derivatives.md`

Add the front matter first, followed by the actual note content.

```markdown
---
layout: page
title: Derivatives
permalink: /subjects/mathematics/calculus/derivatives/
---

# Derivatives

A derivative measures how a function changes
with respect to its input.

## Power Rule

$$
\frac{d}{dx}x^n = nx^{n-1}
$$
```

Commit the file to GitHub. GitHub Pages will rebuild your website and publish the page.

## 3. Creating an Index Page

Use `index.md` for the homepage or an overview page for a subject or topic.

Example path:

`subjects/mathematics/calculus/index.md`

```markdown
---
layout: page
title: Calculus
permalink: /subjects/mathematics/calculus/
---

# Calculus

Explore my calculus notes.

- [Limits](limits.md)
- [Derivatives](derivatives/)
- [Integrals](integrals/)
```

An `index.md` file is not required for every folder. Use it when you want an overview page at that location.

## 4. Naming and Linking Pages

- Use descriptive filenames: `limits.md`, `derivatives.md`, `linear-equations.md`.
- Use `index.md` for landing pages.
- Use Markdown links to connect related pages.
- Use `permalink` when you want to specify a clean, predictable URL.
- Ensure links match the actual published URLs. A link to a directory ending in `/` generally expects an index page at that URL.

## 5. Important Rules

1. Front matter must appear at the very beginning of the file.
2. Use valid YAML syntax and consistent indentation.
3. Put spaces after colons, such as `title: Calculus`.
4. Keep front matter between the opening and closing `---` lines.
5. The layout you specify must exist in your theme.
6. Commit your changes and allow GitHub Pages time to rebuild.

**Basic rule:** Front matter tells Jekyll how to process the page; Markdown contains the actual content of your note.


