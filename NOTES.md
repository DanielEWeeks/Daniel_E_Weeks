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

<https://github.com/sbryngelson/academic-website-template>

and click the "Use this template" button and choose the 'Create a new repository' option.

If you want instead to use my site as a template, you can go to

<https://github.com/DanielEWeeks/Daniel_E_Weeks>

The code there generates this web site:

<https://danieleweeks.github.io/Daniel_E_Weeks/>


# Step 2: Customize the information

To customize it with my own information, I had to modify these files and update some image files.  Initially I changed these, but yet more modifications will be
needed to fully customize it:

```	 
   _config.yml
   _data/funders.yml
   _data/pi.yml
   _pages/home.md
   images/DanWeeks_WordCloud.png
   images/headshot.jpg
```

To add my cv, I made a 'cv' folder, and then copied a PDF of my CV into that folder.  I then edited the 'cv' line in _data/pi.yml as needed.

In _config.yml I turned off some of the pages, like the blog, by putting a hash # sign in front of the line listing them.  I also rearranged the order of the pages.

To customize the listed software, I edited _pages/software.md 

**Customizing References**

Generated a BibTex-formatted set of references from my Zotero database, and pasted them into the assets/ref.bib file.

If the LaTeX tag for the article contains a dash '-' in it, then the BIB and ABSTRACT pop-ups do not work. To get those to work, I had to remove the tags.

For example, this does not work

@article{treble-barna_brain-derived_2023

but this works

@article{treblebarna_brainderived_2023

  
# Step 3: Turn on the GitHub Action

To get it to generate a GitHub Pages website, I then had to follow the instructions here:

<https://jekyllrb.com/docs/continuous-integration/github-actions/>

to change the 

Build and deployment

Source

to 'GitHub Actions'  

using the Deploy Jekyll site to Pages workflow. 


# Generated web site

My generated web site is here:

<https://danieleweeks.github.io/Daniel_E_Weeks/>


# Font Awesome

For the link icons, this uses Font Awesome version 4.2.0.

