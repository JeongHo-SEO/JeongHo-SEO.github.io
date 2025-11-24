# Personal Website

### How to Design
- **index.qmd**: You can write your contents in this file for each folder (sub-pages). (index.md can be also used)

- **_quarto.yml**: YOu can adjust the website design within **Quarto**
    - I used the **Quarto** template (Not jekyll)

### How to build: Use GitHub Actions !!
1. Firstly, change the default settings (main) to gh-pages for **Quarto**
    - Settings > Pages > Source: Deploy from a branch > **Branch: gh-pages** [Not main]

2. Secondly, change the Source to Action
    - Settings > Pages > Source: Github Actions

3. Lastly, create the .yml file for Action Build.
    - .github/workflows/quarto-publish.yml

### Branches
- main: Codes for website
- gh-pages: Quarto automatically renders the website with this branch
