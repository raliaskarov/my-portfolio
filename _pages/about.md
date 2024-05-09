---
layout: home
title: About website
---

I found out about jekyll site generator when scrolling through someone else's portfolio 
so I thought it is good to leave some info here on how to build similar site quite easily.

This website is built using Jekyll which is a library in Ruby to render 
markdown files into html static websites.
You can find out more about Jekyll here:
[github.com/jekyll/jekyll](https://github.com/jekyll/jekyll/)
 and here: [jekyllrb.com/](https://jekyllrb.com/)

Site is set to use jekyll gitbook theme. 
This allows fo friendly sidebar and useful to store large site of a content. 
Find out more about jekyll gitbook at [github.com/sighingnow/jekyll-gitbook](https://github.com/sighingnow/jekyll-gitbook)

Alternatively you can use default theme
[minima](https://github.com/jekyll/minima). 
You can change theme in _conf.yaml file



---
How to launch your own site from scratch using same theme:

Step 1: Create a New Repository on GitHub
*Log in to your GitHub account.
*Click on the "New" button to create a new repository.
*Name your repository <your-username>.github.io (replace <your-username> with your GitHub username).
*Initialize the repository with a README file.
*Click "Create repository".

Step 2: Clone the Repository to Your Local Machine
*Open your terminal or Git Bash.
*Clone the repository using:
```
git clone https://github.com/<your-username>/<your-username>.github.io.git
```

Step 3: Install Jekyll
If you haven't installed Jekyll yet, follow these steps:

Install Ruby and RubyGems (you can check if they are installed by typing ruby -v and gem -v).
Install Jekyll and Bundler:
```
gem install jekyll bundler
```

Step 4: Set Up Jekyll with the GitBook Theme
Navigate into your repository directory:
```
cd <your-username>.github.io
```

Install the Jekyll GitBook theme. You can do this by adding the theme to your Gemfile:
```
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins
gem 'jekyll-gitbook', git: 'https://github.com/sighingnow/jekyll-gitbook'
```
Then run:
```
bundle install
```
Create a new Jekyll site in the same directory:
```
jekyll new --force --skip-bundle .
```
Replace the theme in your _config.yml file with:
```
theme: jekyll-gitbook
```

Add any necessary configuration details from the theme's documentation to your _config.yml.

Step 5: Build and Test Locally
Build your site locally:
```
bundle exec jekyll serve
```

Open your browser and go to http://localhost:4000 to see your new site.

Step 6: Push Changes to GitHub
Add all new files to Git:
```
git add .
```
Commit the changes:
```
git commit -m "Initial Jekyll site with GitBook theme"
```
Push to GitHub:
```
git push -u origin main
```

Step 7: Enable GitHub Pages
Go to your repository on GitHub.
Under your repository name, click on "Settings".
Scroll down to the "GitHub Pages" section.
From the "Source" drop-down, select the branch you want to publish (usually main or master).
Click "Save".
Your site should be available at https://<your-username>.github.io shortly after these settings are saved.
