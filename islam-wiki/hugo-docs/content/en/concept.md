Concept
***********

	* A short title or a name: short description of the period.
	* :doc:`Islam Chronology <../chronology_main>`



## Description

When I only started learning about Biblical and Islamic prophets, I had a hard time trying to figure out the historical order of the stories from ancient books. I had questions like  

The main idea was to gather stories of all prophets mentioned in the Quran and hadith in one page and sort them according a history timeline. 

gathered from various web resources and my notes on Yasir Qadhi's lectures on seerah of the Prophet Muhammad SAW are scattered within corresponding sections. Some info (actually lot of it) is taken from Wikipedia, which is always helpful and well-structured. I tried to remove the parts about prophets that are not mentioned in The Quran or authentic hadiths. Also, I started to create summaries of some sections and reorganize them, but decided to publish it as is hoping that some day I can edit it to the okay state.


Need to do
===========
## STAGE 1. World History Map (General) 
***************************

1. [DONE] Come up with the concept. Some algorithm to make it convenient to read and to support.
	* [DONE] maybe just switch to Hugo as it seems more convenient and versatile:
		* hugo-doks +
		* hugo-book
		* hugo-learn
		* A bad thing about choosing a custom theme is that it may end up not supporting some of the functions that you need and you will learn about it very late in the game and it will be too troublesome to change to some other theme. Also, hugo has documentation, but the themes which in most cases have a bunch of their own code and functions have a very general-level docuentation. I guess mostly because the themes were created by volunteering front-end developers and not by technical writers. that's why these things are smart and dynamic but without instructions.
2. Copy-paste topics.
3. Fact-check and rewrite the topics. 
4. - Buy a hosting place. Just upload to Render.
5. Buy a domain.
5. [DONE] add some images or emoji
6. [DON-] write a disclaimer


## STAGE 2. World History Map (Technical Tasks)

* Need index-numbers and maybe certain div classes for titles and descriptions.
* Send Feedback button
* add favicon
* [DONE] add head menu with links
* [DONE] add custom css
* find how to build a static website with config
	seems like I need to upload it somewhere and fix the baseurl in config before it starts to work locally without serve.
* [DONE] find a way to deal with bootstrap CSS
* [DONE] deal with the TOC (how did I do that?)
* [DONE] attach the upper panel (position: sticky)
* [DONE] expand all toggle (https://stackoverflow.com/questions/43008609/expanding-all-details-tags)
	* Maybe also make this a switch-toggle instead of a button.
* dark mode toggle slider: https://infomate.club/howtoberlin/
* sticky panel include: dark mode toggle, expand all toggle, back to Home link, ?search, ?git link
* change the upper line gradient color
* add a timeline since Ibrahim. now there's no way I can hack bootstrap css on that level
* [DONE] fix CSS for This-Page-TOC background and border in the bootstrap CSS.
* add button to go up to the beginning: 
* [DONE] incorporate search in the current page: https://stackoverflow.com/questions/51988459/html-searching-on-the-same-page/51988637
* put search button inside search field
* -- Try GitLab Pages. Seems like it's free compared to GitHub Pages. (Free but you need to provide your CC data.)
* Do Expand All when clicking a section in the TOC
* [DONE] Create a mockup for timeline-helicopter view of the seerah of Prophet Muhammad sww.


Dark mode switch: https://dev.to/ahmadbassamemran/awesome-animation-checkbox-css-toggle-day-night-mode-5dnm




### Other Stuff
* https://www.islam-guide.com/truth.htm maybe contact them and fix their CSS.
* add the "Useful Links" section


## Notes
* **expand all** script is in layout/docs/single.html
* the menu, buttons, Expand All in the layout/partials/header/header.html
* To fix CSS, use files from the /scss/common directory.
seems like my sense of beauty is inevitably falling behind my willingness to fix all CSS issues.



border-image-source: linear-gradient(
89deg, #067f11e3, #05ffcab3 50%, #4fe622ab);

<label class="switch">
  <input type="checkbox">
  <span class="slider round"></span>
</label>


JS scripts are in single.html. Need to transform them to separate scripts in the js folder.

Wanted to combin the guide from interlinked separate parts where each definition can be source for its own wiki page. hugo has functionality for snippets but seemed like it would require one-level higher content planning and too much overhead so I chose the simplest way.


Sections
===========
1. Ultimate Roadmap of the Universe According to Islam
2. Seerah of the Prophet Muhammad sww with timeline-helicopter view (REST API documentation style) 
2. Interactive chart with the Prophets family.
3. Islam and Science (Scientific Miracles of the Quran)
4. Synopsis for each episode of the seerah of the prophet Muhammad saw
5. Comparison with other religions
6. [God's creation compared to computer programming]
7. Maybe make the interactive chart of connections like in Infinite Jest.

8. Interactive diagram of how persons good and bad deeds are collected by angels and sent to Jannah and Jahannam where they obtain some form.

Custom Header
****************************
* Tabs: 
	* History Map
	* Home
	* Other Stuff
	* Contacts

Databases
****************************
* Prophets
* Sahabi and other important people
* Hadith
* Quran Surahs

An interactive family tree of prophets.
****************************
*  just CSS and HTML: https://codepen.io/Pestov/pen/BLpgm


Nice to Have
****************************


## Hosting

Deploy your static site easily on Render.

Just Link GitLab or GitHub repository, and let it build your website and serve it on a global CDN. The best thing is that static sites are free on Render with no additional cost of up to 100 GB bandwidth a month.