# Personal Website Repository

### Pages
1. Curriculum-Vitae   # CV
2. Papers             # Collaborated Papers
3. Books              # Personally Published 
4. Blog               # Academic Topics
5. Private            # NO Rendering, Do not include in the website
---

### How to Design
- **index.qmd**: You can write your contents in this file for each folder (sub-pages). (index.md can be also used)
- **_quarto.yml**: You can adjust the website design within **Quarto**
    - I used the **Quarto** template (Not jekyll)


### How to build: Use GitHub Actions
<!-- 
- Change the default settings (main) to gh-pages for **Quarto**
    - Settings > Pages > Source: Deploy from a branch > **Branch: gh-pages** [Not main]
--> 
- Change the Source to Action
    - Settings > Pages > Source: Github Actions
- Create the .yml file for Action Build.
    - .github/workflows/quarto-publish.yml


### Branches
- main: Codes for website
- gh-pages: Quarto automatically renders the website with this branch


---
**<p align="right">Lastly Edited: November 24, 2025</p>**
