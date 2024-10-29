# Constructing a Research Group Website

Here's a nice one from today's Biostats Seminar speaker that looks like it works well both on desktop computers and on my cell phone: 

     <https://mzhanglab.github.io/>	  

It uses this template code: 

<https://github.com/sbryngelson/academic-website-template>

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

To customize it with my own information, I had to modify these files and update some image files.  Initially I changed these, but yet more modifications may be
needed to fully customize it:

```	 
   _config.yml
   _data/funders.yml
   _data/pi.yml
   _pages/home.md
   images/DanWeeks_WordCloud.png
   images/headshot.jpg
   _pages/teaching.md
```

Note that the *.yml and *.md files are text files that can be edited online in the GitHub.com website.  The image files can be also added into the appropriate folder in the online interface. 

To add my cv, I made a 'cv' folder, and then copied a PDF of my CV into that folder.  I then edited the 'cv' line in _data/pi.yml as needed.

In _config.yml I turned off some of the pages, like the blog, by putting a hash # sign in front of the line listing them.  I also rearranged the order of the pages.

To customize the listed software, I edited _pages/software.md 

**Turned off pages**

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

