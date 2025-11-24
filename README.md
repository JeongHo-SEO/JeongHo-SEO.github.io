# Personal Website

### How to build
- _quarto.yml: make the website design
    - I used the quarto template (Not jekyll)
- index.qmd: contents in the website (index.md can be also used)

### Use GitHub Actions
1. Settings > Pages > Source: Deploy from a branch > Branch: gh-pages [Not main]
2. Settings > Pages > Source: Github Actions
3. Create the .yml file for Action Build in here: .github/workflows/quarto-publish.yml

Then
- main: for codes
- gh-pages: Quarto makes the website with rendering automatically
