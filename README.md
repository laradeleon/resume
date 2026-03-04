# Hosting a Resume on GitHub Pages

## Purpose

This README is for anyone who wants to publish a formatted resume as a live website and has basic familiarity with Markdown and simple command line steps. By the end of this guide, you’ll have your resume written in Markdown, converted into a website using Jekyll, and hosted publicly on GitHub Pages.

## Prerequisites

Before beginning, make sure you have the following ready:

1. A resume 
    - A plain text or Word version
2. A GitHub account - sign up for free at https://github.com/  
    - GitHub is a platform for hosting code and documents using version control
3. Git - download it at https://git-scm.com/install  
    - Git is the version control software that tracks changes to your files and syncs them with GitHub
4. A Markdown text editor  
    - **Visual Studio Code** - free to download at https://code.visualstudio.com
5. Basic comfort with the terminal (command prompt)  
    - You’ll run a small number of commands, shown exactly as they should be typed

No prior experience with Git, GitHub, or building websites is required.

## Instructions

### Step 1: Create a repository on GitHub

1. Go to [https://github.com](https://github.com) and log in to your account.

2. Click the **+** on the top right corner of the page and select **New repository**

3. In the **Repository name** field, type exactly: `yourusername.github.io`, replacing `yourusername` with your actual GitHub username 
    - e.g., `marvinmclaren.github.io`. 

4. Make sure the **Public** option is selected for the repository's visibility
5. Check the box labelled **Add README**
6. Click **Create repository**


> **Note ("Build a Website"):** Etter recommends hosting documentation on a website instead of distributing it as a PDF. A website will let you fix mistakes right away and ensure that the information stays up to date.
 
---

### Step 2: Clone the repository to your computer

*Cloning* means making a copy of the project onto your computer while keeping it linked to GitHub. This means any changes made can be uploaded back to the website.

1. Open your terminal 
    - **Windows**: search for "Command Prompt"
    - **Mac**: search for "Terminal"

2. Navigate to a folder where you want to store the project. For example, to go to your Desktop folder, type:

```
cd Desktop
```

3. Clone your new repository to your computer by typing:

```
git clone https://github.com/yourusername/yourusername.github.io
```

Replace `yourusername` with your actual GitHub username.

4. Open the project in Visual Studio Code
   - Open **Visual Studio Code**  
   - In the top-left menu, click **File > Open Folder…**  
   - Navigate to the folder named `yourusername.github.io` (the one you just cloned)  
   - Click **Open**

---

### Step 3: Write your resume in Markdown

1. Create a new file in the folder and name it `index.md`
2. Begin your file with the following lines exactly:
   
   ```
   ---
   layout: home
   title: Resume
   ---
   ```

3. Write the content of your resume underneath those lines using Markdown formatting


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

1. Create a new file in your project folder named `_config.yml`
2. Add the following content to the file:

``` yaml
title: "Your Name" # replace this with your actual name
theme: minima # Jekyll's default theme
```



> **Note ("Make Static Websites"):** A *static site generator* like Jekyll takes your Markdown file and your chosen theme and creates a website with the specified styling. Unlike dynamic websites that require a database and a running server to generate pages, a static site is prebuilt HTML that's served directly to your browser. This makes it faster and simpler to maintain.

--

### Step 5: Commit and push your files to GitHub

*Commit* means creating a “snapshot” of your work. This is like a saved checkpoint we can return to later. *Push* is uploading that snapshot to GitHub so it appears online. Once the `index.md` and `_config.yml` files are saved, the next step is to send those changes to GitHub so the website can update.

1. In Visual Studio Code, open the built‑in terminal:  
   - Go to the top menu and select **Terminal > New Terminal**.

2. In the terminal that appears at the bottom of VS Code, type:

   ```
   git add .
   ```
   This tells Git to include all the new and changed files in the next save point.
2. Commit (save) your changes with a short description:
   ```
   git commit -m "Add resume and Jekyll config"
   ```
3. Push (upload) your changes to GitHub:
   ```
   git push
   ```

> **Note ("Publish Frequently"):** Etter emphasizes that publishing should not be a special event and it should be quick. The three commands above (`add`, `commit`, `push`) is all that's need to update your live website. 

## Step 6: View your website

Wait up to two minutes after pushing. GitHub Pages may need a minute or two to build the website after receiving new files.

1. Open a web browser and navigate to: `https://yourusername.github.io`


2. You should see your resume rendered!

> **Note:** If changes do not appear right away, wait two minutes and try again. If the problem persists, try refreshing the page: `Ctrl + Shift + R` on Windows or `Cmd + Shift + R` on Mac.

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

## Credits

This README was written for COMP 2600: Technical Communication in Computer Science, Winter 2026, University of Manitoba.

**Peer review contributors:**
- Ill add this later...

**Third‑party content:**
- Jekyll Primer theme, licensed under the MIT License: https://github.com/pages-themes/primer
- Jekyll Minima theme, licensed under the MIT License: https://github.com/jekyll/minima
- Andrew Etter, *Modern Technical Writing* (2016)
- William S. Pfeiffer, *Technical Communication: A Practical Approach*
