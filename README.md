# julius-lab.github.io

## Preamble
This repo powers the updated Julius Lab homepage. If you're a member of the Julius Lab and need to edit the website, you're probably already part of the Github organization. If not, reach out to Dr. Julius or Chukwuemeka to get added to the organization. Once you're part of the organization, you should be able to edit this repo (please be careful with this power). Now onto the meaty stuff.

This tutorial assumes you're familiar with Github repos in general. If not, here's a [handy guide](https://docs.github.com/en/get-started/quickstart/hello-world#making-and-committing-changes). You should make all your changes on the main branch of this repo, but please make sure no one is working on the site when you want to (I suggest asking in the lab's WebEx first).

## Installing Jekyll
The website is powered by [Jekyll](https://jekyllrb.com), which you'll use to build the site locally before uploading here. To use Jekyll easily, you'll need a Linux or MacOS setup. The Windows setup is a little more complicated, but still possible. You can also use the new [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/about). It'll let you use Linux directly on your Windows system and you won't need a whole extra OS.

Once you've picked OS, here's [how to install Jekyll](https://jekyllrb.com/docs/installation/). After installing Jekyll, you can clone this repo into a folder on your system. 

There's a [step-by-step tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/) on Jekyll if you'd like to know more about the process.


## Editing the Site
This section goes over the things that I changed for our site. If I didn't touch it, you can assume I know nothing about it. There's a nice guide from the original source of the layout available [here](https://academicpages.github.io/markdown/) if you're curious. 

To change basic site-wide aspects, there are three places of interest. The first two probably don't need much changing, but they're detailed here for completeness.

### Site-Wide Configuration
**_config.yml** is where the basic configuration options go. Going through the file should be self-explanatory. It's also got the information that shows up in the sidebar - profile links, logo, site title, etc. 

For example, to edit the lab's side-bar description, edit the author.bio part of the file.

### Top Navigation Bar
To change the nav bar, edit _data/navigation.yml. Each item in the file shows up in the top navigation bar. The order matters here. Once you've added a page to the nav bar, you need to make sure it exists following the information in [Pages](#pages).

### Pages
To add or remove site pages, edit the _pages/ folder. Pages can be either markdown or html, and adding them to the folder makes them available for linking within the site. The following list has all the pages.
1. All the site's pages currently used are in the _pages/ folder and named:
    1. about.md (home page)
    2. research.html
    3. people.md
    4. teaching.html
    5. publications.html
2. The supporting files are in the folders:
    1. images/ - Image assets
    2. files/ - Papers and syllabi in PDF form can go here
3. The file for the **Sidebar** is _includes/sidebar.html. I couldn't see a reason to touch this.
4. The **Site footer**. This currently just has the copyright and necessary attributions.
    1. _includes/footer.html
    2. _includes/footer/custom.html

To edit any page, use the appropriate syntax for the language, and then build the site using the commands [here](#building-the-site).


## Building the Site
When editing the site, you can host it locally to see how your changes are taking shape. To host it, run
```bash
bundle exec jekyll serve --livereload
```
from within the site's root folder. The site should then be running on your localhost. Just type in "localhost:4000" in your browser to see it. The ```--livereload``` flag means the site should be building as you save edits. 

Another option to just build the site once is:
```bash
JEKYLL_ENV=production bundle exec jekyll build
```
After either command is done, the site is built into the _site/ folder. You can then add, commit, and push the updated repo to finish updating the site. Once the repo is updated, Github Pages takes care of updating the live website.


## General Tips
1. Name a file “.md” to have it render in markdown, name it “.html” to render in HTML.

## Links
1. [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/about)
2. [Jekyll step-by-step tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/)
3. [Academic Pages](https://academicpages.github.io/markdown/)
4. [Liquid syntax guide](https://shopify.github.io/liquid/tags/control-flow/)
5. [Github Guide](https://docs.github.com/en/get-started/quickstart/hello-world#making-and-committing-changes)


## Credits
The entire website is based on the Github Pages template for academic websites from [here](https://github.com/academicpages/academicpages.github.io). Excerpt from the repo's README:
> This was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License. See LICENSE.md. 