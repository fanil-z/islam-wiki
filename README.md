
# Description

Chronology of Islam (from creation of the Earth and till recent years)

# Instructions

## Dependencies

* node.js (This will automatically install npm.)

## Building Website

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

### Note on CSS

THe website wouldn't get the bootstrap css from @hyas node on production builds. I don't know how to fix it, so I just implemented added an additional custom CSS file in the head.html. Using this approach I can actually just use a simple hugo theme and bump the CSS there. I don't know. 

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


# Test Environment

Test version of the website is published on Render: https://islam-wiki.onrender.com/docs/wiki/islam-wiki

