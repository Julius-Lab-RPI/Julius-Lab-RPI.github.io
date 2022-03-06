# julius-lab.github.io


## Usage Tutorial
There's a nice guide from the original source of the layout available [here](https://academicpages.github.io/markdown/). This tutorial goes over the things that I changed for our lab. If I didn't touch it, you can assume I know nothing about it.

The page is powered by Jekyll.

To change basic site-wide aspects, there are three places of interest
### Site-Wide Configuration
_config.yml is where the basic config options should go. Going through the file should be self-explanatory.

### Top Navigation Bar
To change the nav bar, edit _data/navigation.yml. Each item in here shows up in the top navigation bar.

### Single Pages
To add or remove site pages, edit the _pages/ folder. Pages can be either markdown or html, and adding them to the folder makes them available for linking within the site.

All the pages currently used are in the _pages/ folder
1. about.md (home page)
2. research.html
3. publications.html
4. teaching.html
5. people.md

Folders for supporting files:
1. images/ - Image assets
2. files/ - Papers and syllabi in PDF form can go here

Sidebar:
_includes/sidebar.html

Edit site footer:
_includes/footer.html
_includes/footer/custom.html

## General Tips
1. Name a file “.md” to have it render in markdown, name it “.html” to render in HTML.
2. d

## Links
1. [Liquid syntax guide](https://shopify.github.io/liquid/tags/control-flow/)
2. d


## Credits
The entire website is based on the Github Pages template for academic websites from [here](https://github.com/academicpages/academicpages.github.io). Excerpt from the repo's README:
> This was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License. See LICENSE.md. 