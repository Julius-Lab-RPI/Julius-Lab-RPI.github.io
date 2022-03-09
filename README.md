# julius-lab.github.io

This repo powers the new Julius Lab homepage. If you're a part of the Julius Lab and need to edit the website, you're probably already part of the Github organization. If not, reach out to Dr. Julius or Chukwuemeka to get added to the organization. Once you're part of the organization, you should be able to edit this repo (please be careful with this power). Now onto the meaty stuff.


## Installing Jekyll
The website is powered by [Jekyll](https://jekyllrb.com), which you'll use to build the site locally before uploading here. To use Jekyll easily, you'll need a Linux or MacOS setup. The Windows setup is a little more complicated, but still possible. You can also use the new [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/about). It'll let you use Linux directly on your Windows system and you won't need a whole extra OS.

Once you've picked OS, here's [how to install Jekyll](https://jekyllrb.com/docs/installation/). After installing Jekyll, you can clone this repo into a folder on your system. 

There's a [step-by-step tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/) on Jekyll if you'd like to know more about the process. 


## Building the Site
When editing the site, you can host it locally to see how your changes are taking shape. To host it, run
```bash
bundle exec jekyll serve --livereload
```
from within the site's root folder. The site should then be running on your localhost. Just type in "localhost:4000" in your browser to see it. 


## Editing the Site
This section goes over the things that I changed for our site. If I didn't touch it, you can assume I know nothing about it. There's a nice guide from the original source of the layout available [here](https://academicpages.github.io/markdown/) if you're curious. 

To change basic site-wide aspects, there are three places of interest. The first two probably don't need much changing, but they're detailed here for completeness.

### Side-Bar
_config.yml is where the basic configuration options go. Going through the file should be self-explanatory. It's got mostly information that shows up in the sidebar - profile links, logo, site title, etc.

### Top Navigation Bar
To change the nav bar, edit _data/navigation.yml. Each item in the file shows up in the top navigation bar. The order matters here. You

### Single Pages
To add or remove site pages, edit the _pages/ folder. Pages can be either markdown or html, and adding them to the folder makes them available for linking within the site. 

All the site's pages currently used are in the _pages/ folder and named:
1. about.md (home page)
2. research.html
3. people.md
4. teaching.html
5. publications.html

Folders for supporting files:
1. images/ - Image assets
2. files/ - Papers and syllabi in PDF form can go here

Sidebar:
_includes/sidebar.html

Edit site footer:
_includes/footer.html
_includes/footer/custom.html

To edit any, use the appropriate syntax for the language, and if you'd already run the command [here](#building-the-site), the site should be building as you save edits. Another option to just build the site is:
```bash
JEKYLL_ENV=production bundle exec jekyll build
```
After either command is done, the site is built into the _site/ folder. You should commit and push the updated repo to finish updating the site. Once you've pushed the 



## General Tips
1. Name a file “.md” to have it render in markdown, name it “.html” to render in HTML.

## Links
1. [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/about)
2. [Jekyll step-by-step tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/)
3. [Academic Pages](https://academicpages.github.io/markdown/)
4. [Liquid syntax guide](https://shopify.github.io/liquid/tags/control-flow/)


## Credits
The entire website is based on the Github Pages template for academic websites from [here](https://github.com/academicpages/academicpages.github.io). Excerpt from the repo's README:
> This was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License. See LICENSE.md. 