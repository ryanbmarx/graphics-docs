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
