---
title: 'Developing Academic Website Using GitHub Pages and Jekyll'
date: 2024-11-09
permalink: /posts/2024/11/creating_your_website/
excerpt_separator: <!--more-->
tags:
  - webpage
  - academic pages
  - github
  - git 
---

This is a blog on a workshop that I'll be teaching to University of Arizona School of Plant Sciences Graduate students and Post-doctoral researchers. I'll add more content next week


# Workshop: Build Your Academic Website with GitHub Pages and Jekyll

## Overview
Welcome to the workshop on building your own academic website using GitHub Pages and Jekyll! This guide will take you through the process step-by-step, accommodating users on Windows, Ubuntu, and macOS.

### Workshop Outline
1. **Introduction and Overview**
2. **Setting Up GitHub and Installing Prerequisites**
3. **Creating Your GitHub Repository**
4. **Choosing and Setting Up a Jekyll Theme**
5. **Adding Content: Publications, CV, and Blog Posts**
6. **Deploying the Website on GitHub Pages**
7. **Customizing Further: Adding Plugins and Features**
8. **Q&A and Troubleshooting**
9. **Wrap-up and Resources**

---

## 1. Introduction and Overview
- Objective: Understand the importance of an academic website, GitHub Pages, and Jekyll.
- Examples: Professional academic websites.
- Activity: View a live academic website built with GitHub Pages.

---

## 2. Setting Up GitHub and Installing Prerequisites

### Step 1: Set Up GitHub
1. Go to [GitHub](https://github.com) and create an account if you don’t have one.
2. Download and install **Git**:
   - **Windows**: Download from [Git for Windows](https://git-scm.com/download/win) and follow the installation steps.
   - **macOS**: Install via Homebrew (`brew install git`) or download from [Git for macOS](https://git-scm.com/download/mac).
   - **Ubuntu**: Run `sudo apt update && sudo apt install git`.
3. Configure Git with your GitHub credentials:
   ```
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```

### Step 2: Install Ruby and Jekyll
1. Install **Ruby**:
   - **Windows**: Use [RubyInstaller](https://rubyinstaller.org/).
   - **macOS**: Install via Homebrew (`brew install ruby`).
   - **Ubuntu**: Run `sudo apt update && sudo apt install ruby-full`.
2. Install **Jekyll** (run the following command in your terminal):
   ```
   gem install jekyll bundler
   ```

---

## 3. Creating Your GitHub Repository

1. Log in to GitHub and create a new repository. Name it in the format `your-username.github.io`.
2. Clone the repository to your local machine:
   ```
   git clone https://github.com/your-username/your-username.github.io.git
   ```
3. Navigate into the repository:
   ```
   cd your-username.github.io
   ```

---

## 4. Choosing and Setting Up a Jekyll Theme

### Step 1: Download a Jekyll Theme
1. Choose a theme like [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/).
2. Download the theme and extract its contents into your GitHub repository folder.

### Step 2: Customize `_config.yml`
1. Open the `_config.yml` file and edit your personal details, such as:
   - **Name**
   - **Email**
   - **Social media links**
2. Run the site locally to test:
   ```
   jekyll serve
   ```
   - **Windows**: Run the command from the Command Prompt or PowerShell.
   - **macOS/Ubuntu**: Run from the Terminal.
3. Visit `http://localhost:4000` in your browser to preview the site.

---

## 5. Adding Content: Publications, CV, and Blog Posts

### Step 1: Add a Publications Page
1. Create a new file in the `_pages` directory named `publications.md`.
2. Add your publication details in markdown format.

### Step 2: Set Up Your CV
1. Create a `cv.md` file and link your CV PDF.
2. Add it to the navigation bar in `_config.yml`.

### Step 3: Write a Blog Post
1. Create a new file in the `_posts` folder with the naming format: `YYYY-MM-DD-title.md`.
2. Write your blog post using markdown.

---

## 6. Deploying the Website on GitHub Pages

1. Commit your changes:
   ```
   git add .
   git commit -m "Initial setup of the academic website"
   git push origin main
   ```
2. Go to the repository settings on GitHub and set the source to the main branch.
3. Access your live site at `https://your-username.github.io`.

---

## 7. Customizing Further: Adding Plugins and Features

1. Install plugins such as **Google Analytics** or **social sharing buttons**:
   - Add the plugin to your `Gemfile` and `_config.yml`.
   - Run `bundle install` to install the plugins.
2. Experiment with other features like image galleries or integrating ORCID.

---

## 8. Q&A and Troubleshooting
- Common issues: Missing dependencies, configuration errors, and troubleshooting theme display problems.
- Open Q&A session to address participant questions.

---

## 9. Wrap-up and Resources
- **Recap**: Steps covered during the workshop.
- **Resources**: Links to Jekyll documentation, GitHub Pages guides, and community forums.
- **PDF Guide**: [Download the full workshop guide](#).

Thank you for participating in the workshop!