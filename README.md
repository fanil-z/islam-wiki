
### Table of contents
------------------------

<!--ts-->
   * [Overview](#overview)
   * [🛠 Tech Stack](#-tech-stack)
   * [💚 How to Contribute](#-how-to-contribute)
   * [Additional Technical Instructions](#additional-technical-instructions)
<!--te-->

# Overview

World History Timeline according to Quran, hadiths,  (from creation of the Earth and till the Day of Judgement and beyond).

☪️ WEBSITE: [gilmetdeen.com](https://gilmetdeen.com/islam-wiki/)

![Website layout](https://github.com/fanil-z/islam-wiki/blob/master/website-layout.png?raw=true)

# 🛠 Tech Stack

TLDR: Hugo, Hyas, Node.js

![Stack](https://github.com/fanil-z/islam-wiki/blob/master/tech-stack.png?raw=true)

1. **Hugo**: a static web-site generator that builds a static HTML/CSS/JS website using MD files as a source. It is open-source, flexible; it has a large number of themes including themes for user manuals and API references. Hugo can be a good candidate if you use Markdown and want to implement the docs-as-code concept in your documentation department.
	- **Hyas**: I used the Hyas theme to have a good-looking bootstrap layout.
		- Hyas depends on Node.js and a swarm of npm packages. On Windows, you will also need Chocolatey to configure it.
		- **Doks** theme. I had to add and tune some JS/CSS elements to adjust the website to my purposes. Doks is a bit too advanced for a beginner like me so I still have plenty of bugs to fix. There are standard Hugo themes that can be configured in 5 min.
2. **Render**: I am hosting the website on Render. Up to 100GB bandwith and 400 total build hours is free of charge. I also tried Netlify, basically the same functionality.
3. A pipeline on Render fetches the latest commit in my git repo, installs all required npm packages, builds the website and pushes it to production. You can configure a test server on Render but I just test on my local machine.

Content of the website is written in Markdown: [./hugo-docs/content](https://github.com/fanil-z/islam-wiki/tree/master/hugo-docs/content)

# 💚 How to Contribute

Contributions are very welcome! 

1. Clone the repo.

		git clone https://github.com/fanil-z/islam-wiki.git

2. Write your post OR edit/proofread an existing content in the [Markdown](https://www.markdownguide.org/basic-syntax/) format. Put your source files in the [./hugo-docs/content](https://github.com/fanil-z/islam-wiki/tree/master/hugo-docs/content) directory.

3. Commit + push changes to your branch and create a pull request.

I will try to approve ASAP. After the merge, the Render pipeline will fetch the latest commit, rebuild the website and republish it.

## 🤷 I Want to Contribute but I don't know what to do

* Proofreading
* Collecting sources
* If you have some valuable knowledge or expertise in any Islamiic topic, please share it and write a post.

# Additional Technical Instructions

## Building Website Manually

1. Clone the repo.

		git clone https://github.com/fanil-z/islam-wiki.git

2. Install npm dependencies.

    	cd hugo-docs
    	npm install

3. To build the website on a local machine, run the following command.
	
	    npm run start /local serve

4. To build the website with the production configuration, run the following: 

	    npm run build /production

## Updating Dependencies

    npm update

## Editing CSS

To edit CSS settings, change the `\islam-wiki\hugo-docs\static\css\custom.css` file.

Note: when you fix the bug with not fetching css on production, you can edit the css directly in '\assets\scss\common' instead of using custom css.

### Note on CSS [Bug!]

The website wouldn't get the bootstrap css from @hyas node on production builds. I don't know how to fix it, so I just implemented added an additional custom CSS file in the head.html. Using this approach I can actually just use a simple hugo theme and bump the CSS there. Need to fix this issue anyway.

### Summary Before Marker Color

Change the stroke color in manual-add.css

```
summary::before{display:inline-block;content:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' width='14' height='14' viewBox='0 0 16 16'%3e%3cpath fill='none' stroke='grey'...
```

## Adding JS Scripts

JS scripts are in `single.html`. Need to transform them to separate scripts in the js folder.

## TOC Settings

Change the config/default/markup.html file.

[tableOfContents]
  endLevel = 4
  ordered = false
  startLevel = 1

### Disabling TOC

To disable the TOC, add the following in the front matter of the page.

	---
	toc: false
	---
