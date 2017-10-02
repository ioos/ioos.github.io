---
title: Getting started with IOOS Documentation Theme
keywords: sample homepage
tags: [getting_started, about, overview]
sidebar: mydoc_sidebar
topnav: topnav
toc: false
search: exclude
#permalink: index.html
summary: These brief instructions will help you get started quickly with the IOOS Documentation Theme for Jekyll.
---


## Building a Documentation Site with the Theme

Follow these instructions to build the new documentation site on GitHub Pages with the IOOS Documentation Theme for Jekyll adapted for IOOS specifics. The [IOOS Documentation Theme for Jekyll](https://github.com/ioos/documentation-theme-jekyll) is a fork of the original ["Documentation Theme for Jekyll"](https://github.com/tomjohnson1492/documentation-theme-jekyll) modified for the IOOS specifics. 

This single IOOS theme was developed to streamline and simplify management of the IOOS documentation sites hosted on GitHub Pages. When a new IOOS documentation site is built following the instructions described here,
it will provide a consistent look and feel across all of IOOS' project documentation sites, and will simplify the process
to update the template across each site if needed.  

This is accomplished by using the git _**'submodule'**_ concept, which allows each individual documentation site to reference this template for the Jekyll boilerplate code.  Updating the theme for each downstream documentation site can be accomplished by a **`git submodule update [--remote --merge]`** command, rather than separately modifying
the Jekyll boilerplate code to match in each.  

## Getting the IOOS Documentation Theme

Deploying this template for your own IOOS-branded GitHub Pages documentation site can be done in a couple different ways, which mainly differ from each other in whether the Jekyll development environment is set to run locally for more rapid iterative markdown/content update, or the GitHub Pages' own Jekyll framework is used to render updates (GitHub Pages internally uses Jekyll to render HTML from markdown).  The latter approach allows to just copy the content of the skeleton theme repository into your own repository 'gh-pages' branch, make a few config file modifications, and push to GitHub directly to see a rendered site matching exactly this site without any special software on your workstation (other than perhaps a GitHub client for pushing updates to GitHub).

In the event that the documentation site had already been deployed, and all it takes is just a minor text update, it can be done by editing the content markdown files content directly on GitHub with a browser; no software installation is required in such case. 

### STEP 1. Local Jekyll Development

<!-- <br>
{::nomarkdown}<p style="color:blue; font-size:120%; border:3px solid red; padding:15px; text-align:center"> If you can't run Ruby/Jekyll on your workstation, go to Step 2 </p>{:/}
<br> -->

Running Jekyll locally will allow for faster site development, but you need to install Ruby on your workstation. If you are able to run the Ruby/Jekyll environment locally, refer to the comprehensive instructions provided in the [Installation section](http://idratherbewriting.com/documentation-theme-jekyll/mydoc_about_ruby_gems_etc.html) of the Jekyll Documentation Theme. More details can be found on the web pages from the Reference section below.

### STEP 2. Download and install the theme

If you can't run Ruby/Jekyll on your workstation, you can still make a GitHub Pages documentation site based on this
template.  The process to do this is to download the code from the 'gh-pages' branch of the "IOOS Documentation Theme for Jekyll" repository, adapt for your site needs, and publish to a 'gh-pages' branch of your own repository. 

Depending on how familiar you are with the 'git' software, and whether you already have GitHub repository that just need to be wrapped into IOOS theme, you may choose one of the following paths:

#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2a. Conversion of the existing GitHub repository to the IOOS Documentation Theme

First download the theme from the [Github repo](https://github.com/ioos/documentation-theme-jekyll): 

```
cd /my/sourcecode/dir
git clone --recursive -b gh-pages https://github.com/ioos/documentation-theme-jekyll
cd documentation-theme-jekyll
```

Next, you will need to copy the files downloaded to the 'documentation-theme-jekyll' directory to your target repository. For an existing repository, the easiest way to do this is to create a new 'gh-pages' branch, and then remove all git-tracked files and replace by the template code.  Roughly, this looks like (use with caution):

```
cd /my/target/repository
git checkout -b gh-pages master
git rm -r *
git rm .*
```
Then copy the content of the 'documentation-theme-jekyll' repository into you target repository, and add all the files to git for tracking **`git add --all`**. Once you have the code in hand, instructions below describe relevant files to modify to adapt the template to your needs.

When you've made changes and you would like to see how they look on your GitHub Pages site, simply commit and push them up to your existing GitHub repository:

```
git commit -a -m "Initial GitHub Pages site built using 'IOOS Documentation Theme'"
git push origin gh-pages
```

#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2b. Publishing a new GitHub documentation site with the IOOS Documentation Theme 

First you need to create a new target repository. For example, you created a repository 'my-new-doc-repo' in the IOOS organization on GitHub.

Next, you need to mirror a bare-bone repository 'ioos-documentation-jekyll-skeleton' that includes all necessary file templates onto the newly created repository:  

``` 
git clone --bare -b gh-pages https://github.com/ioos/ioos-documentation-jekyll-skeleton.git
cd sos-guidelines-jekyll.git
git push --mirror -b gh-pages https://github.com/ioos/my-new-doc-repo.git
```

That's it. You now have a bare-bone documentation repository on GitHub that you can clone to your local computer and modify in accordance with the instructions in the following sections:

```
git clone --recursive -b gh-pages https://github.com/ioos/my-new-doc-repo
```

## Modifying Theme Content For Your Site

The important files and directories to modify the template are the following:

|**Name**|**Description**|
|--------|------------|
|\_config.yml | Main Jekyll configuration files.  Modify settings in these to change anything related to the theme.  The important settings to update are primarily located at the top of the file, and include settings like: 'title', 'name', 'description', 'baseurl', among others.  More documentation can be found in the 'Documentation Theme for Jekyll' original documentation (see below).|
|/\_data/topnav.yml| Configuration file for a top navigation menu (most likely, the default version will not require any change at all) |
|/\_data/sidebars/mydoc_sidebar.yml| Configuration file for a side accordion navigation menu.  Further description of the configuration details and how they work is beyond the scope here, refer to the Jekyll and the 'Documentation Theme for Jekyll' original documentation for more info.|
|/\_docs/| Directory to place any GitHub-standard markdown content to publish|
|/\_docs/index.md| This markdown file that contains the content for the 'homepage' for the site|

- All published documents in Markdown must be placed into the '_docs' directory, where they can be edited with any true text editor such as 'vi', 'emacs', 'notepad', 'notepad++', etc.  
- Alternatively,  if you just need to edit a document or two on the existing site, you may do that directly on GitHub with your browser in 3 simple steps:
   1. Go to the page you want to edit, and click on the "Edit me" button just below the page Title and Summary;
   2. Open it for editing by clicking on the "pencil" icon at the right side above the file content;
   3. Make all changes, preview them to make sure that everything is OK, and commit them to the 'gh-pages' (make sure that the "Commit directly to the gh-pages branch" option is checked).

  >**Important Note:** in order to keep the local copy of the repository in sync with directly updated remote one, you must run the following commands:
  >
  >```
  >git fetch
  >git reset --hard origin/[branch-you-made-changes-on] 
  >```    

### Configuring side navigation bar

The sidebar navigation adapts to the documentation. Although the theme allows to use several sidebars (see `_config.yaml` file), a single sidebar 'mydoc_sidebar' is used by default for IOOS implementation. The sidebar name must be specified in a page's frontmatter. Here's an example of the page frontmatter showing the sidebar property:

```
---
title: Alerts
tags: [formatting]
keywords: notes, tips, cautions, warnings, admonitions
last_updated: July 3, 2016
summary: "You can insert notes, tips, warnings, and important alerts in your content. These notes are stored as shortcodes made available through the linksrefs.hmtl include."
<span class="red">sidebar: mydoc_sidebar</span>
permalink: mydoc_alerts
---
```

The `sidebar: mydoc_sidebar` refers to the `\_data/sidebars/mydoc_sidebar.yml` file. The sidebar data file uses a specific YAML syntax that you must follow. Follow the sample pattern shown in the theme, specically looking at `mydoc_sidebar.yml` as an example.

For more details on the sidebar syntax, see [Sidebar navigation](http://idratherbewriting.com/documentation-theme-jekyll/mydoc_sidebar_navigation.html).

### Configuring top navigation bar

The top navigation usually remains the same, because it allows users to navigate across other sites. The top navigation works just like the sidebar. You can specify which topnav data file should load by adding a `topnav` property in the document `frontmatter`, like this:

```
topnav: topnav
```

Here the `topnav` refers to the `\_data/topnav.yml` file. Most likely, there will be no need to edit the default `topnav.yml` file included into the theme template.

### Editing Markdown documents 

This theme uses [kramdown markdown](http://kramdown.gettalong.org/), which is similar to Github-flavored Markdown.

Every document must start with the so-called frontmatter properties:

```
---
title: "Some title"
tags: [sample1, sample2]
keywords: keyword1, keyword2, keyword3
last_updated: Month day, year
summary: "optional summary here"
sidebar: sidebarname
topnav: topnavname
toc: false
#search: exclude
#permalink: filename.html
---
```

For titles, surrounding the title in quotes is optional, but if you have a colon in the title, you must surround the title with quotation marks. If you have a quotation mark inside the title, escape it first with a backlash `\`.

Values for `keywords` get populated into the metadata of the page for SEO.

Values for `tags` must be defined in your \_data/tags.yml list. You also need a corresponding tag file inside the tags folder that follows the same pattern as the other tag files shown in the tags folder. (Jekyll won't auto-create these tag files.)

In the current version of the theme, the `permalink` property value interferes with other collection settings; therefore it should be commented in the frontmatter. However, it should not be removed as it may be needed in future versions.

Value for `search` controls inclusion of the document content into theme search mechanism. If you want to be able to perform basic search through your site documents, make sure that this property is commented in the frontmatter. 

Follow the sample pattern shown in the theme, specifically looking at Markdown sample documents in the `_docs` folder as an example.

### Updating theme templates  

This operation should be performed whenever you modify the content of your site in order to sync it with the IOOS Documentation Theme updates  

```
 git submodule update --remote --merge
```

## References  

 - [Original Documentation for the Documentation Theme for Jekyll](http://idratherbewriting.com/documentation-theme-jekyll/index.html)
   - [Ruby & Jekyll Installation and Setup Section](http://idratherbewriting.com/documentation-theme-jekyll/mydoc_about_ruby_gems_etc.html) 
 - [A Comprehensive Guide for Jekyll](https://jekyllrb.com/docs/home/)
 - [Ruby documentation & downloads](https://www.ruby-lang.org/en/)
    - [Ruby Installer for Windows](http://rubyinstaller.org/downloads/)
    - [A Guide on Ruby Installation and Setup for Windows 10](https://www.digitalocean.com/community/tutorials/how-to-install-ruby-and-set-up-a-local-programming-environment-on-windows-10)
 - [General information on the way GitHub uses Jekyll in 'GitHub Pages' sites](https://help.github.com/articles/about-github-pages-and-jekyll/)
    - [In particular, how to use a specially-named branch 'gh-pages' to push documentation for a 'Project' page (which most repos will fall under)](https://help.github.com/articles/user-organization-and-project-pages/)

