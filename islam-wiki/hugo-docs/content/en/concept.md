Concept
***********

	* A short title or a name: short description of the period.
	* :doc:`Islam Chronology <../chronology_main>`

Need to do
===========
* Need to come up with some algorithm to make it convenient to read and to support.
* Need index-numbers and maybe certain div classes for titles and descriptions.
* background-color
* Send Feedback button
* Buy a hosting place.
* add favicon
* add head menu with links
* add custom css
* find how to build a static website with config
* [DONE] maybe just switch to Hugo as it seems more convenient and versatile:
	* hugo-doks +
	* hugo-book
	* hugo-learn
* https://www.islam-guide.com/truth.htm maybe contact them and fix their CSS.
* add the "Useful Links" section
* add some images or emoji
* find a way to deal with bootstrap CSS
* [DONE] deal with the TOC (how did I do that?)
* [DONE] attach the upper panel (position: sticky)
* put the search-box to the upper level
* transfer the history roadmap from /docs to the /wiki folder.
* [DONE] expand all toggle (https://stackoverflow.com/questions/43008609/expanding-all-details-tags)
* dark mode toggle slider: https://infomate.club/howtoberlin/
* sticky panel include: dark mode toggle, expand all toggle, Home link, ?search, ?git link
* write the disclaimer
* change the upper line gradient color
* add a timeline since Ibrahim. now there's no way I can hack bootstrap css on that level
* seems like I need to upload it somewhere and fix the baseurl in config before it starts to work locally without serve.
* [DONE] fix CSS for This-Page-TOC background and border in the bootstrap CSS.
* add button to go up to the beginning: 
* incorporate search in the current page: https://stackoverflow.com/questions/51988459/html-searching-on-the-same-page/51988637
* put search button inside search field
* Try GitLab Pages. Seems like it's free compared to GitHub Pages.

To fix CSS use files from the /scss/common directory.
seems like my sense of beauty is falling behind my willingness to fix all CSS issues.


## Notes
* **expand all** script is in layout/docs/single.html
* the menu, buttons, Expand All in the layout/partials/header/header.html

so, I did some calculations and if I have 1000views in a month for 30 years, I will need to start to pay.


border-image-source: linear-gradient(
89deg, #067f11e3, #05ffcab3 50%, #4fe622ab);

<label class="switch">
  <input type="checkbox">
  <span class="slider round"></span>
</label>


Sections
===========
1. Ultimate Roadmap of the Universe According to Islam
2. Interactive chart with the Prophets family.
3. Islam and Science (Scientific Miracles of the Quran)
4. Synopsis for each episode of the seerah of the prophet Muhammad saw
5. Comparison with other religions
6. [God's creation compared to computer programming]
7. Maybe make the interactive chart of connections like in Infinite Jest.


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




Example
.. _chronology_main:
Section to cross-reference
--------------------------
This is the text of the section.
It refers to the section itself, see :ref:`chronology_main`.
:doc:`Islam Chronology <../chronology_main>` 

Bismilah
