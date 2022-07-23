Concept
***********

	* A short title or a name: short description of the period.
	* :doc:`Islam Chronology <../chronology_main>`

>npm run build /production 
>npm run start /local serve
>npm update

updated npm packages and somehow fixed the bug with css not compiling.
cloudflare pages

## Description


Hello everyone and assalamu aleikum,

In my current workplace, I learned about a static HTML generator Hugo. 

It's open source, flexible, has a large number of themes including themes for user manuals and API references.

In order to get some Hugo and CSS practice, I started wrapping up my notes about Islam into a static website, carried away and after only one year spending about 15min daily the MD editor showed it will take about 8 hours to read the whole page.
When I only started learning about Biblical and Islamic prophets, I had a hard time trying to figure out the historical order of the stories from ancient books. After several years of googling nub questions like 'Was Solomon before Moses?' or 'When Soddom and Gomorra happened?' my notes and tables started to grow. That's why the main idea was to gather and currate stories of all prophets mentioned in the Quran and sahih hadith in one page and sort them according to a historical timeline.
Another aspect that always bothers me in large documentation samples is that it is not so easy to create a proper helicopter view of the whole thing. TOC helps you to navigate but doesn't give a summary. However in terms of history TOC can actually kind of give you a short description of what happened. Trying to combine the helicopter view and large portions of text, I've used the standard <details><sumamry> tags so that details about a historic event appears when you click on the topic.




While trying to tune the CSS, it made me kind of start loving front-end and I learned how to implement the dark mode along the way.
There are still tonnes of bugs and I quickly realized that my sense of beauty is not enough to fix all CSS issues.


1. Markdown: the content is written in Markdown files + with some HTML additions.
2. GitLab: source files for content + CSS, JS, themes are stored in GitLab.
3. Hugo: a static web-site generator builds a static HTML/CSS/JS website using MD files as a source.
	- Hyas: I used Hyas to have a good-looking, neat bootstrap layout. 
		- Hyas depends on Node.js. I installed it on my laptop.
		  Node.js is easy to install on Linux and probably Mac. On Windows, you will also need Chocolatey.
	- Doks theme
		- CSS: The theme is cool but I needed to adjust is to my purposes. So, I added the custom CSS file (~150 lines).
		- JS: added buttons for sending feedback, expanding/hiding details elements all at once, in-page search and dark mode switch toggle.
		- Hugo is super-flexible and has a large amount of useful features but at the beginning it was hard to navigate through all the functionality and figure out which exactly config files I had to change. Hugo documentation is helpful here.
4. Render or Netlify: static web-files are hosted in Render. up to 100GB is free.
Generated website is uploaded to a production GitLab repo; Render checks if there is an update in the repo and automatically updates the content.
5. I bought the domain here:
6. Scripting. Wrote a basic bash script that pushed latest changes in the source, triggers Hugo to generate the website and pushes to production. Yes, I test on production.

Hugo has good documentation, but custom themes mostly written by front-end enthusiasts almost don't have documentation, which leaves you to reverse engineer the setup. I wouldn't recommend Hyas/Doks for beginners or if you want to customize the layout or CSS, there are much simpler themes of Hugo that can be configured in 5 min.

gathered from various web resources:
Islam: A Short History by Karen Armstrong who is a famous historian and a Christian nun.
my notes on Yasir Qadhi's lectures on seerah of the Prophet Muhammad SAW are scattered within corresponding sections. Some info (actually lot of it) is taken from Wikipedia, which is always helpful and well-structured. I tried to edit them a little, remove the parts that are not mentioned in The Quran or authentic hadiths. Also, I started to create summaries of some sections and reorganize them, but decided to publish it as is hoping that some day I can edit it to the okay state. 
The bad thing I noticed about Wikipedia is there are a lot of articles written not by Islamic scholars but by Eastern 

Please use the Send feedback button if the order is not correct or if you find something conradicting the Quran or authentic hadith.

Probably I won't be able to finish the whole thing if the content was not about Islam that is exciting to explore. However the most painful part was to gather information on the First Fitnah and how the era of righteous khalifs came to an end after assassination of Ali. Even though the Golden Age of Islam starts right after, for me it is the saddest periods of Islamic history, when we can say that the original ummah of the Prophet Muhammad ceased to exist. May Allah forgive us and guide us to the right path.

I also had to spend additional time adding a cat 🐈 every time the name of noble Abu Huraira comes up because, verily, Abu Huraira that stands for "Father of a kitten" in Arabic. was truly worht it.

After realizing that you can do so many things without a web server but just with HTML, CSS and JavaScript, I really started to like the simplicity of what's happening behind the building and hosting process.
Well, maybe the fact that I know very little about building a web server plays a significant role here as well.

I really need to finish the Eschatonian part, for now it's hard to figure out the order of events in the signs of Day of Judgement and Al Qiyamah itself.

The main page markdown file is 5000 lines. Islam teaches to finish what you started, so I tried to spend on this at least 10 minutes a day. Slowly it got into shape, Alhamdulillah. I had some good time trying to gather particles of an endless puzzle.
but there are still many bugs left.S
I have many doubts like was Thamud earlier than 'Ad or vice versa.

hugo is a good choice if you want to implement docs-as-code approach and if the documentation team is ready to work with markdown instead of some traditional XML editor.
I've been editing raw markdown files for a while until I found about https://github.com/marktext/marktext which is open source and really nice. has a spell checker.

https://github.com/mundimark/awesome-markdown-editors

90k words, 6000 paragraphs.
My Ghostwriter editor says the reading time of the whole thing is 6 hours. I wonder how much time I've spent there.

https://miro.com/app/board/o9J_kqBzhXk=/

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