#How to start a project
## Get assignment, collect information, brainstorm until you have an idea
## Decide what format it should be
* **Digital first:** This should be thought through before the print graphic. 
* Your primary options
  - **Static:** Reserved for simple charts (1-2 per image). When a chart has little value standing alone, an embeddable static graphic is a good choice.
  - **Graphics gallery:** This can be very effective in situations where the charting is copious but not complex. Like static graphics, galleries are embeddable within stories. Polls are very successful in this format.
  - **HTML story:** If the idea is text-heavy, more complex than a simple chart and/or has interactive opportunities choose an HTML story.
  - **Tarbell app:** With greater capabilities within NGUX, tarbell projects have a very high bar. THe project should require tons of custom elemtns and/or have a long shelf life. All Tarbell apps also require P2P story link assets and a URL redirect.
* The skedmaker will make a best guess at a format on the daily graphics sked, but it's usually only a guess. Gather some data. Learn something. If you think an alternate format is better, then say so. Make sure there isn't a bigger plan.
* **Digital first:** This should be thought through before the print graphic. 

## So you've decided to make static graphics.
* Use the .AI template. This is the 16x9 graphic.
* Be mindful of the inner margin if making a gallery.
* Duplicating the artboard in a single AI file makes it easier to output (and reoutput) graphics. Especially galleries or items with repeated elements such as headers.
* Output as **full-res JPEGs**. P2P will do all the web-friendly processing.
* Keep them simple and free of most decorations and text. Two charts max.
* These should be made with an eye toward embedding. As little text as possible. Text trapped in images is bad, so let's keep it to a minimum
* As long as you stick to the template, mobile design isn't a big deal. The template is made for this.

## HTML stories
* If it doesn't work on mobile, then it doesn't work.
* Sketch this out, even in really basic ways.
* Sketch the desktop version, too. (See what i did there?)
* Text on images is bad. It doesn't scale well and is unreadable to visually-impaired readers. As much text as possible — including headers, labels, etc. — should be in HTML.
* Diagrams: In most cases, use numbers/letters with a corresponding ordered list.
* Use a proper text editor ([TextWrangler](http://www.barebones.com/products/textwrangler/), [TextMate](http://macromates.com/), [Sublime Text](http://www.sublimetext.com/)). Do not use a rich-text editor like Microsoft Word, Text Edit or even Illustrator. This will cause you more problems than it solves. 
* [Download the startup template](http://photodesk.chicagotribune.com.s3.amazonaws.com/graphics-toolbox/graphics-html-story-template.zip)
  + It's a ZIP on S3.
  + Always start with it, so upgrades/changes can be made.
  + Practice semantic coding:
    - [Code Academy](http://www.codecademy.com/) has some essential tutorials for HTML, CSS, Javascript and many other.
    - Tables are not design tools. Use the zebra figure:
      ```
      	<figure class='zebra'>
		<figcaption>This is the header for the list</figcaption>
		<ul>
			<li><p><strong>Optional header</strong> sit amet, coli</p></li>
			<li><p>Lorem in st laborum.</p></li>
			...
		</ul>
	</figure>
      ```
    - New legend format: _(example forthcoming)_
  + Get it workin pretty good off your desktop, then put it in p2p. There will inevitbaly be tweaks needed, though the template tries to minimize that The more you communicate about issues you have the better the template will become.
* We have some nice tools to use, but they might not be needed. You don't need to use every crayon in your box every time. We have a clicker, but is that needed. What about sortable/searchable tables? Is that functionality critical or at least transformative? 

## So you've decided on a tarbell app. 
* There are no guidelines. This is a pure custom job and you should work with Ryan on it. Move along.

## Editing
* Reporter must see the content.
* Late editor must see the content. At this stage, it's a pretty good idea to make sure Ryan sees it, too, even if he isn't the editor.
* If printing, previewing and/or emailed PDFs are not viable distribution options, then check "no index, no follow" and make it live. This should be a temporary solution (mere hours). ![Scereenshot of a P2P edit screen](http://photodesk.chicagotribune.com.s3.amazonaws.com/graphics-toolbox/documentation/no-index-no-follow.png)


## Fill out p2p fields
* Use your name, if you like, but include your own Twitter handle. _Have you set your P2P defaults?_
* **Slug** should be SEO 
  ![Screenshot of a P2P edit screen](http://photodesk.chicagotribune.com.s3.amazonaws.com/graphics-toolbox/documentation/slug.png) 

* **Headline** should be sexy, and SEO if possible. 
  ![Screenshot of a P2P edit screen](http://photodesk.chicagotribune.com.s3.amazonaws.com/graphics-toolbox/documentation/headline.png)

* **SEO headline**, **SEO description** should be boring and front-loaded with search terms. 
  ![Screenshot of a P2P edit screen](http://photodesk.chicagotribune.com.s3.amazonaws.com/graphics-toolbox/documentation/seo-headline.png)

* **SEO keywords:** Up to ten, seperated by commas. One of them should be "onlinegraphic" 
  ![Screenshot of a P2P edit screen](http://photodesk.chicagotribune.com.s3.amazonaws.com/graphics-toolbox/documentation/keywords.png)

* **Thumbnail. Thumbnail. Thumbnail:** Should be representative of the graphic, but not necessarily a screengrab. p2p does soft crops on them, so any objecitonable material should be cropped in photoshop. 
  ![Screenshot of a P2P edit screen](http://photodesk.chicagotribune.com.s3.amazonaws.com/graphics-toolbox/documentation/thumbnail.png)

* Should be **related/embedded** to main story if at all possible. 
  ![Scereenshot of a P2P edit screen](http://photodesk.chicagotribune.com.s3.amazonaws.com/graphics-toolbox/documentation/related.png)

## Wrapping up:
* Email to skedmaker: 
  - Slug
  - Status (Live, working but ready, working awaiting edits, needs relating, etc.)
  - Copy desk status (which editor has it?)
  - Any embargoes. These are your responsilibity.
  - A suggested tweet/shareline.
* Communicate with both Jonathon/Ryan and the *zzctc-ctweb* and *Ct-digital-editors* when assets are ready and if they will need to be flipped live.
* Tweet it: Put it out there, then we can grab it and reshare.



