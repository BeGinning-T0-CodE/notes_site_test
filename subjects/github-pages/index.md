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


