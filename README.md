# Hosting a Resume on GitHub Pages

## Purpose

This guide is for anyone who wants to publish a resume as a live website. It assumes basic familiarity with Markdown and simple command‑line steps. By the end, you will have written your resume in Markdown, applied a Jekyll theme, and published the site publicly using GitHub Pages.

## Prerequisites

Before beginning, make sure you have the following ready:

1. A resume 
    - A plain text or Word version
2. A **GitHub** account - sign up for free at https://github.com/  
    - GitHub is a platform for hosting code and documents using version control
3. **Git** - download it at https://git-scm.com/install  
    - Git is the version control software that tracks changes to your files and syncs them with GitHub
4. A Markdown text editor  
    - **Visual Studio Code** - free to download at https://code.visualstudio.com
5. Basic comfort with the terminal (command prompt)  
    - You’ll run a small number of commands, shown exactly as they should be typed

No prior experience with Git, GitHub, or building websites is required.

## Instructions

### Step 1: Create a repository on GitHub

1. Go to [https://github.com](https://github.com) and log in to your account

2. Click the **+** on the top right corner of the page

3. Select **New repository**

3. In the **Repository name** field, type exactly: `yourusername.github.io`, replacing `yourusername` with your actual GitHub username 
    - e.g., `marvinmclaren.github.io`. 

4. Make sure the **Public** option is selected for the repository's visibility
5. Check the box labelled **Add README**
6. Click **Create repository**


> **Note ("Build a Website"):** Etter recommends hosting documentation on a website instead of distributing it as a PDF. A website will let you fix mistakes right away and ensure that the information stays up to date.
 
---

### Step 2: Clone the repository to your computer

*Cloning* means making a copy of the project onto your computer while keeping it linked to GitHub. This means any changes made on your computer can be uploaded back to GitHub.

1. Open the search bar on your computer

2. Type **Command Prompt** (Windows) or **Terminal** (Mac) and open the application

3. Navigate to a folder where you want to store the project. For example:
```
cd Desktop
```

4. Clone your repository by typing the following, and replacing `yourusername` with your actual GitHub username.:

```
git clone https://github.com/yourusername/yourusername.github.io
```


5. Open **Visual Studio Code**  
   - Click **File** in the top-left menu
   - Click **Open Folder**
   - Find the folder that was created when you ran the `git clone` command. It will be named `yourusername.github.io`
   - Select that folder and click **Open** 

---

### Step 3: Write your resume in Markdown

1. Create a new file in the folder and name it `index.md`
2. Add the following lines at the top of the file:
   
   ```
   ---
   layout: home
   title: Resume
   ---
   ```

3. Write the content of your resume underneath those lines using Markdown


A short example looks like this:

``` markdown
# Marvin McLaren

## Education

**MBA - University of Manitoba** (2013)

## Experience

**Finance Manager - Foomatic** (2003–Present)
- Managed quarterly budgets and financial assets
- Led a team of five analysts
```

> **Note ("Use Lightweight Markup"):** Etter argues that documentation should live online and tools like Microsoft Word or HTML make this difficult. Microsoft Word mixes content and styling and isn’t free or available on all systems. Alternatively, lightweight markup languages, like Markdown, avoid these problems as they’re plain text, free to use, and separate the content from design. This makes them better suited for creating documentation.


### Step 4: Configure Jekyll with a theme

GitHub Pages uses Jekyll automatically so no installation is required. Only a small configuration file needs to be added.

1. Create a new file in your project folder and name it `_config.yml`
2. Add the following content to the file:

``` yaml
title: "Your Name" # replace this with your actual name
theme: minima # Jekyll's default theme
```


> **Note ("Make Static Websites"):** A static site generator, like Jekyll, takes your Markdown file and your chosen theme and creates a website with the specified styling. Unlike dynamic websites that require a database and a running server to generate pages, a static site is prebuilt HTML that's served directly to your browser. This makes it faster and simpler to maintain.

---

### Step 5: Commit and push your files to GitHub

*Commit* means creating a “snapshot” of your work. This is like a saved checkpoint we can return to later. *Push* is uploading that snapshot to GitHub so it appears online. Once the `index.md` and `_config.yml` files are saved, the next step is to send those changes to GitHub so the website can update.

1. Open **Visual Studio Code**

2. Open the built‑in terminal by clicking **Terminal** in the top menu


3. Click **New Terminal**

4. Type:

   ```
   git add .
   ```

5. Commit your changes by typing:
   ```
   git commit -m "Add resume and Jekyll config"
   ```
> **Note:** The text inside the quotes is the *commit message*, a short description that explains what changes you made in that commit.


6. Push (upload) your changes to GitHub by typing:
   ```
   git push
   ```

## Step 6: View your website

Wait up to two minutes after pushing. GitHub Pages may need a minute or two to build the website after receiving new files.

1. Open a web browser and navigate to: `https://yourusername.github.io`


2. You should see your resume rendered!

## Further Resources/Readings

- [**Markdown Tutorial**](https://commonmark.org/help/tutorial/) (CommonMark)
    - An interactive guide that teaches the basics of writing in Markdown
- [**GitHub Pages**](https://docs.github.com/en/pages)
    - Explains how GitHub Pages works, how your site is published and how to customize it
- [**Git Guides**](https://github.com/git-guides)
    - Explanations of Git concepts like commits, branches, and pushing changes
- [**Jekyll Documentation**](https://jekyllrb.com/docs) 
    - Covers how Jekyll builds your site, how themes work, and how to customize layouts

- [**Jekyll Theme Collection**](https://github.com/topics/jekyll-theme) (GitHub)
    - A gallery of free Jekyll themes

## Frequently Asked Questions

**Why is Markdown better than writing raw HTML for a resume?**

Writing in HTML requires you to wrap every piece of content in tags. For example, a heading would look like `<h2>Experience</h2>`, and a bulleted list would require several nested tags for each item. This clutters the file and makes it harder to read your content while you are editing. Markdown reads naturally in any text editor, even before it is converted to a website. As Etter describes, lightweight markup keeps the writers focused on the content, not the syntax.

**I updated my resume in Markdown and pushed the changes to GitHub. Why don't I see the changes when I refresh the website in my browser?**

There are two possible causes. First, GitHub Pages needs about one to two minutes to rebuild your site after you push your changes. If you refresh immediately, you may still see the previous version. Second, your browser may have cached a local copy of the old page. Force it to load the most recent version by refreshing: `Ctrl + Shift + R` on Windows or `Cmd + Shift + R` on Mac. 


## Credits

This README was written for COMP 2600: Technical Communication in Computer Science, Winter 2026, University of Manitoba.

**Peer review contributors:**
- Eunice Taborlupa
- Palak Patel

**Third‑party content:**
- Jekyll Primer theme, licensed under the MIT License: https://github.com/pages-themes/primer
- Jekyll Minima theme, licensed under the MIT License: https://github.com/jekyll/minima
- Andrew Etter, *Modern Technical Writing* (2016)
- William S. Pfeiffer, *Technical Communication: A Practical Approach*
