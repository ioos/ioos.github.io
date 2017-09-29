---
title: Jekyll Installation and Setup
keywords: sample Jekyll development
tags: [getting_started, about, overview]
sidebar: mydoc_sidebar
topnav: topnav
toc: false
search: exclude
#permalink: index.html
summary: These abridged instructions will help you with installation and setting up Jekyll on your computer. Following these instructions, including the Jekyll dependency installation, will provide you a full development environment necessary to run the site.
---

### Requirements/References: ###

- Ruby: [https://www.ruby-lang.org/en/](https://www.ruby-lang.org/en/), Windows users:
  [Ruby Installer for Windows](http://rubyinstaller.org/downloads/)
- Jekyll: [https://jekyllrb.com/](https://jekyllrb.com/) (for reference, no need to download as it's available as a Ruby gem)
- Minimal Mistakes Jekyll theme: [https://mmistakes.github.io/minimal-mistakes/](https://mmistakes.github.io/minimal-mistakes/)

### Installation:

- Install Ruby for your environment (via package manager(Unix) or installer (Windows)).  See instructions on the Ruby site.
- Install Jekyll in your Ruby environment:

```
      gem install jekyll
```

- The _**Documentation Theme for Jekyll**_ recommends installing Bundler for dependency management to run Jekyll more easily.  See the [install docs](http://idratherbewriting.com/documentation-theme-jekyll/mydoc_about_ruby_gems_etc.html) for more info.

```
      gem install bundler
```

- Clone the ioos_jekyll_theme GitHub repo ('gh-pages' branch) to get this example code. This will include a git submodule reference to the 'master' branch which includes the theme itself.  

```
cd /my/sourcecode/dir
git clone --recursive -b gh-pages https://github.com/ioos/ioos_jekyll_theme.git
cd ioos_jekyll_theme
```

- Install dependencies via Bundler:

```
bundle install
```

- From here, you should be able to run Jekyll to preview the site using the commands below.  Different options listed in the three command examples below highlight the development settings available in Jekyll for verbose logging and watching for code changes as you edit markdown files and automatically recompiling the HTML for preview.  

```
bundle exec jekyll serve
bundle exec jekyll serve --watch --verbose
bundle exec jekyll serve --watch --verbose --incremental
```

Out of the box, this will publish a local Jekyll service listening on port 4000, with the site available at this URL:

[http://localhost:4000/ioos_jekyll_theme/](http://localhost:4000/ioos_jekyll_theme/)

The path the site is deployed to should be modified to match your repository name by changing the 'baseurl' setting
 in the \_config.yml (primary Jekyll config/GitHub Pages deployment settings file) and the \_config_dev.yml
(local development settings override) files.



============================================

### 2. Install Jekyll

If you've never installed or run a Jekyll site locally on your computer, follow these instructions to install Jekyll:

* [Install Jekyll on Mac][mydoc_install_jekyll_on_mac]
* [Install Jekyll on Windows][mydoc_install_jekyll_on_windows]

### 3. Install Bundler

In case you haven't installed Bundler, install it:

```
gem install bundler
```

You'll want [Bundler](http://bundler.io/) to make sure all the Ruby gems needed work well with your project. Bundler sorts out dependencies and installs missing gems or matches up gems with the right versions based on gem dependencies.

### 4. Option 1: Build the Theme (*without* the github-pages gem) {#option1}

Use this option if you're not planning to publish your Jekyll site using [Github Pages](https://pages.github.com/).

Bundler's Gemfile is how it specifies and manages project dependencies are managed. Although this project includes a Gemfile, this theme doesn't have any dependencies beyond core Jekyll. The Gemfile is used to specify gems needed for publishing on Github Pages. **If you're not planning to have Github Pages build your Jekyll project, delete these two files from the theme's root directory:**

* Gemfile
* Gemfile.lock

If you've never run Jekyll on your computer (you can check with `jekyll --version`), you may need to install the jekyll gem:

```
gem install jekyll
```

Now run jekyll serve (first change directories (`cd`) to where you downloaded the project):

```
jekyll serve
```

### 4. Option 2: Build the Theme (*with* the github-pages gem) {#option2}

If you *are* in fact publishing on Github Pages, leave the Gemfile and Gemfile.lock files in the theme.The Gemfile tells Jekyll to use the github-pages gem. **However, note that you cannot use the normal `jekyll serve` command with this gem due to dependency conflicts between the latest version of Jekyll and Github Pages** (which are noted [briefly here](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/)).

You need Bundler to resolve these dependency conflicts. Use Bundler to install all the needed Ruby gems:

```
bundle update
```

Then *always* use this command to build Jekyll:

```
bundle exec jekyll serve
```

If you want to shorten this long command, you can put this code in a file such as jekyll.sh (on a Mac) and then simply type `. jekyll.sh` to build Jekyll.

## Running the site in Docker

You can also use Docker to directly build and run the site on your local machine. Just clone the repo and run the following from your working dir:

```
docker build --no-cache -t mydocs .
```

Once the build is complete, you can mount and run the whole site as follows:

```
docker run -v "$PWD:/src" -p 4000:4000 mydocs serve -H 0.0.0.0
```
This is perhaps the easiest way to see how your site would actually look.
