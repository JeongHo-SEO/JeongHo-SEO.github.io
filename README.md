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
         │    │    ├─ _metadata.yml     # Do NOT Create this file. [However, I did... for dividing into categories in my blog.]
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

### SEO(Search Engine Optimization) set-up
1. Enroll our root-url in [Google Search Console](https://search.google.com/search-console/welcome). In this case, use the "URL 접두어".
2. Now, we have to add our html tag. Since I used the ***_quarto.yml*** file for design my website, I had two tasks.
    - I created **new html file** and wrote my html tag. (google-verification.html)
    - Then, I added the **html file** in the bottom of my ***_quarto.yml*** file. (include-in-header: google-verification.html)
3. Add the **site-url: "your-website-link"** in the website section of ***_quarto.yml*** file. e.g.,
    ```
    website:
        title: "JeongHo SEO"
        site-url: "https://jeongho-seo.github.io"  # for google Sitemaps
    ```
4. From above, the Quarto automatically create two files.
    - (1) sitemap.xml file. For example, "https://jeongho-seo.github.io/sitemap.xml".
    - (2) robots.txt file. For example, "https://jeongho-seo.github.io/robots.txt".
5. Lastly, in the "Google Search Console > 색인생성 > Sitemaps", you can add your own Sitemap. Just insert the "sitemap.xml" in the blank.

---
**<p align="right">Lastly Edited: November 27, 2025</p>**
