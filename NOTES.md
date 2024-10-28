# Constructing a Research Group Website

Here's a nice one from today's Biostats Seminar speaker that looks like it works well both on desktop computers and on my cell phone: 

     <https://mzhanglab.github.io/>	  

It uses this template code: 

<https://github.com/sbryngelson/academic-website-template>


# Step 1: Copy the template to your own GitHub account

Log into GitHub in your web browser.

Go to 

<https://github.com/sbryngelson/academic-website-template>

and click the "Use this template" button and choose the 'Create a new repository' option.


# Step 2: Customize the information

To customize it with my own information, I had to modify these files and update some image
files:

```	 
   _config.yml
   _data/funders.yml
   _data/pi.yml
   _pages/home.md
   images/DanWeeks_WordCloud.png
   images/headshot.jpg
```
  
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

