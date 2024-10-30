# Constructing a Research Group Website

Here's a nice one from today's Biostats Seminar speaker that looks like it works well both on desktop computers and on my cell phone: 

     <https://mzhanglab.github.io/>	  

It uses this template code: 

<https://github.com/sbryngelson/academic-website-template>

I started with this template code, but it has subsequently been customized and
extended as described below.

# Step 0: Create a GitHub account

Create a GitHub account at <https://github.com/>.


# Step 1: Copy the template to your own GitHub account

Log into GitHub in your web browser.

Go to 

<https://github.com/DanielEWeeks/Daniel_E_Weeks>

and click the "Use this template" button and choose the 'Create a new repository' option.

The code there generates this web site:

<https://danieleweeks.github.io/Daniel_E_Weeks/>


# Step 2: Customize the information

The majority of the customization can be done by editing *.yml and *.md text files, and by copying desired image files into the 'images' folder, copying an updated CV into the 'cv' folder, etc.   

However, some of the customizations required using some HTML (For example, see the Syllabus button links in _pages/teaching.md or the publication search links at the start of _pages/publications.md).  Some of these links were copied from my Department of Human Genetics faculty page. 

To customize it with my own information, I had to modify these files and update some image files.  Initially I changed these, but yet more modifications may be
needed to fully customize it:

```	 
   _config.yml
   _data/funders.yml
   _data/pi.yml
   _data/news.yml
   _pages/home.md
   images/DanWeeks_WordCloud.png
   images/headshot.jpg
   _pages/teaching.md
   _pages/publications.md 
```

Note that the *.yml and *.md files are text files that can be edited online in the GitHub.com website.  The image files can be also added into the appropriate folder in the online interface. 

To add my cv, I made a 'cv' folder, and then copied a PDF of my CV into that folder.  I then edited the 'cv' line in _data/pi.yml as needed.

To customize the listed software, I edited _pages/software.md 

**Turned off pages and adjusted page order**

In _config.yml I turned off some of the pages, like the blog, by putting a hash # sign in front of the line listing them.  I also rearranged the order of the pages.

Note that I edited the _config.yml to turn off these three pages:

```
# - name: talks
# - name: research
# - name: blogs
```

If you wish to have these pages in your web site, remove the hash # sign and then edit accordingly. 

**Customizing References**

Generated a BibTex-formatted set of references from my Zotero database, and pasted them into the assets/ref.bib file.

If the LaTeX tag for the article contains a dash '-' in it, then the BIB and ABSTRACT pop-ups do not work. To get those to work, I had to remove the tags.

For example, this does not work

@article{treble-barna_brain-derived_2023

but this works

@article{treblebarna_brainderived_2023


As I don't have many conference proceedings, I deleted this

```
<div class="jumbotron">
### Refereed conference proceedings
{% bibliography --query @inproceedings %}
</div>
```

from _pages/publications.md 

If the BibTex entry starts with the

@unpublished{}

tag instead of @article{}, it will be listed in the Preprints section of the Publications page.



**Customizing Academic Icons**

To add an ORCiD academic icon, I had to import the css for

<https://jpswalsh.github.io/academicons/>  

into _includes/head.html, and then adjust accordingly in 

```
_includes/sidebar.html
_pages/about.md
_pages/team.md
```

After these adjustments, then changing the ORCiD link only requires you adjust the 'orcid' line in _data/pi.yml:  

orcid: https://orcid.org/0000-0001-9410-7228

**Customizing favicon.ico**

I put my own favicon.ico in the root directory - this is the little icon that appears in the upper right of the web page.

Pitt has University of Pittsburgh favicon.ico files, but we are only permitted to use them on web sites that end in *.pitt.edu. 

I think if you don't have a favicon.ico that you'd like to use, you can probably simply delete it.  

  
# Step 3: Turn on the GitHub Action

To get it to generate a GitHub Pages website, I then had to follow the instructions here:

<https://jekyllrb.com/docs/continuous-integration/github-actions/>

to change the 

Build and deployment

Source

to 'GitHub Actions'  

using the Deploy Jekyll site to Pages workflow. 

This should automatically update the github.io website after each update is committed.  


# Generated web site

My generated web site is here:

<https://danieleweeks.github.io/Daniel_E_Weeks/>


# Font Awesome

For the link icons, this uses Font Awesome version 4.2.0.

