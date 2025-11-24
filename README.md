# Personal Website Repository

### Pages (for personal)
    1. Curriculum-Vitae   # CV
    2. Papers             # Collaborated Papers
    3. Books              # Personally Published 
    4. Blog               # Academic Topics
    5. Private            # NO Rendering, Do not include in the website

### How to Design - Have to Be Created
- **.github/workflows/Quarto-Publish.yml**: Use this file for **Actions**
- **index.qmd**: You can write your contents in this file for each folder (sub-pages). (index.md can be also used)
- **_quarto.yml**: You can adjust the website design within **Quarto** in this file for root.
    - I used the **Quarto** template (Not jekyll)
    - You can choose the Theme in [Bootswatch](https://bootswatch.com/)
    - Read my _quarto.yml in the root directory for understanding.
- If you want to **change the design in your sub-website**, you have to create a **_metadata.yml** file in the sub-folder.(OverRide the _quarto.yml)
    - theme, format, navbar...
    - ***Caution***: You Do Not Create several *_metadata.yml* in your deep sub-folders. Only one sub-folder is admitted.
        ```
         ├─ _quarto.yml
         ├─ index.qmd
         ├─ A folder
         │    ├─ _metadata.yml
         │    ├─ index.qmd
         │    ├─ B folder
         │    │    ├─ index.qmd
         │    │    ├─ _metadata.yml     # Do NOT Create this file
        ```

### How to build: Use GitHub Actions
- Choose the Source to Action.
    - Settings > Pages > Source: Github Actions
- Copy and Paste the "_quarto.yml" and "deploy-quarto.yml" files.
- Create the folders which you want, then write the contents in the "index.qmd".


### Branches
- main: Codes for website
- gh-pages: Quarto automatically renders the website with this branch


### Notes
- If the website renders the "README.md" file or cannot render anything,
    1. Change the settings > Pages > Deploy from a branch: None
    2. Change the settings > Pages > Deploy from a branch: gh-pages
    3. Change the settings > Pages > Actions (again trial)
---
**<p align="right">Lastly Edited: November 24, 2025</p>**
