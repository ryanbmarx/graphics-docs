
#What do you want to do?
Add the following items to the very top of your HTML page. Each script/link need only be used once. If, fpr example, you're combining two different tools rquiring jQuery, then you need only to paste the script once.

##Start with our base CSS
	
	<link rel="stylesheet" type="text/css" href="http://photodesk.chicagotribune.com.s3.amazonaws.com/graphics-toolbox/tribune-graphics-base-1.0.min.css">
##<a name="static-table"></a>Make a standard table
Tables are NOT design tools They should not be used to organize anything a normal perosn wouldn't normally handle in a spreadsheet. If you feel like you need a table, you probably want a [bullet box](#bulletbox) instead. To ensure the table properly responds to mobile devices, each `<td>` element should employ a `data-title` attribute containing the associated column header. To easily make a standard table in our responsive style (cribbed from NPR), use our custom [tableizer][tableizer] which gives you a basic format like this: 
	
	<table id='' class=''>
		<thead>
			<tr>
				<th>Header 1</th>
				<th>Header 2</th>
				<th>Header 3</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td data-title='Header 1'>XXX</td>
				<td data-title='Header 2'>YYY</td>
				<td data-title='Header 3'>ZZZ</td>
			</tr>
			<tr>
				<td data-title='Header 1'>AAA</td>
				<td data-title='Header 2'>BBB</td>
				<td data-title='Header 3'>CCC</td>
			</tr>
			<tr>
				<td data-title='Header 1'>DDD</td>
				<td data-title='Header 2'>EEE</td>
				<td data-title='Header 3'>FFF</td>
			</tr>
		</tbody>
	</table>

##Make an interactive table?
You'll need these javascript libraries

	<script type='text/javascript' src="http://code.jquery.com/jquery-2.1.1.min.js"></script>
	<script type='text/javascript' src="//cdn.datatables.net/1.10.2/js/jquery.dataTables.min.js"></script>
	<script type='text/javascript' src="//cdn.datatables.net/responsive/1.0.1/js/dataTables.responsive.js"></script>

You'll need these css libraries:

	<link rel="stylesheet" type="text/css" href="//cdn.datatables.net/1.10.2/css/jquery.dataTables.min.css">
	<link rel="stylesheet" type="text/css" href="//cdn.datatables.net/responsive/1.0.1/css/dataTables.responsive.css">
	<link rel="stylesheet" type="text/css" href="//photodesk.chicagotribune.com.s3.amazonaws.com/Graphics/graphics-libraries-no-delete/tribune-datatables.css">
Use our custom [tableizer][tableizer] to easily make the table. No need to use the `data-title` attribute as we would with [static tables](#static-table). 

The interactive table has a completely different system for being responsive. If you find that your columns aren't sorting properly, or want them to sort in a way that's different than the cells content, you can add a `data-order` attribute, which takes priority when sorting. For instance, a column with dollar figures and a couple of "n/a" or other notes would sort in alphabetical order not numerical order (because of the text). Commas, percent signs and dollar signs do not disrupt sorting. Use the `data-order` attribute to give numerical values for the cell. For instance, this table will sort alphabetically

	<table id='' class=''>
		<thead>
			<tr>
				<th>Name</th>
				<th>Salary</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td>John</td>
				<td>$1,000,000</td>
			</tr>
			<tr>
				<td>Jon</td>
				<td>$1.3 million</td>
			</tr>
			<tr>
				<td>Milton</td>
				<td>n/a</td>
			</tr>
		</tbody>

	</table>

Using the `data-order` attribute, we can sort the table using the cells' dollar values (with -1 standing in for the n/a so it sorts last).


	<table id='' class=''>
		<thead>
			<tr>
				<th>Name</th>
				<th>Salary</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td>John</td>
				<td data-order=1000000>$1,000,000</td>
			</tr>
			<tr>
				<td>Jon</td>
				<td data-order=1300000>$1.3 million</td>
			</tr>
			<tr>
				<td>Milton</td>
				<td data-order=-1>n/a</td>
			</tr>
		</tbody>

	</table>

##<a name='bulletbox'></a>Bullet box
Often times we have multiple short blurbs/nuggets that need a home. Use this zebra'ed bullet box. It's part of the base css. Add a class of 'zebra' to add the blue stripes

	<figure class='bulletbox zebra'>
		<figcaption>This is the header for a list</figcaption>
		<ul>
			<li>
				<p><strong>Optional strong leadin</strong> sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat nonproident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
			</li>
			...
		</ul>
	</figure>
We also have a variant that is well-suited for quick hit pairs, such as height: XX, width: XX, speed: XX, etc. It's called a definition list

	<figure class='bulletbox'>
		<figcaption>This is a list without a zebra</figcaption>
		<dl>
		  <dt class=''>Label</dt>
		  <dd class=''>Description</dd>
		  <dt class=''>Label2</dt>
		  <dd class=''>Description2</dd>
		  ...
		</dl>
	</figure>


##Make a templated design
This is another one of those things that you should work with Ryan on.

	<script type='text/javascript' src="http://code.jquery.com/jquery-2.1.1.min.js"></script>
	<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/underscore.js/1.7.0/underscore-min.js"></script>
##Use the "clicker," a.k.a. makePanels.js
You'll need these javascript libraries:

	<script type='text/javascript' src="http://code.jquery.com/jquery-2.1.1.min.js"></script>
	<script type="text/javascript" src='http://photodesk.chicagotribune.com.s3.amazonaws.com/Graphics/graphics-libraries-no-delete/makePanels/jquery.makePanels.1.0.min.js'></script>
You'll need this css libraries:
	
	<link rel="stylesheet" type="text/css" href="http://photodesk.chicagotribune.com.s3.amazonaws.com/Graphics/graphics-libraries-no-delete/makePanels/jquery.makePanels.1.0.min.css">
Structure your HTML like this:

	<div id='something-unique'>
		<div id='something-else-unique' class='panel' data-btn-lbl ='This is the label'>
		...
		</div>
	</div>
The overall wrapper needs a unique ID, as does each panel within it. The `data-btn-lbl` attribute for each panel is the text that will be used in the buttons or dropdown menu.

Use this javascript. Generally, all your javascript need only be inside one `<script>` tag

	<script type="text/javascript">
	$('#something-unique').makePanels({
		type:"dropdown", 	/* Options are "none", "buttons" or "dropdown" */
		transitionSpeed: 150, /* 0=instant, 1000 = 1 second */
		showForwardBackButtons:true, /* duh! */
		alignNav:"center" /* Also can be "left" */
	});
	</script>
##A standard timeline 
We have the tarbell-based timeline (ex. [red light tickets](http://graphics.chicagotribune.com/news/local/red-light-timeline/)), but without a shelf-life these are too laborius for the payoff. For most cases, especially those with just text and photos, use this format. It's built into the Tribune Graphics's base CSS and only requires a wrapper.
	
	<section class='timeline'>
		<div class='timeline-module '>
			<h4>DATE DATE DATE</h4>
			<p>Caption or blurb can go above or below optional photo(s)</p>
			<figure>
				<img src='path/to/photo' alt='Alternate text' />
				<figcaption>This is the caption</figcaption>
			</figure>
		</div>
		...
	</section>

##Colors

**NGUX:**

+ <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#12182D;'></span>Right rail blue:#12182D

**GRAPHICS:**

* **Blues:**
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#144a7c;'></span>Trib blue (NGUX): #144a7c
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#7493C1;'></span>Trib blue 2: #7493C1
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#CBDDED;'></span>Trib blue 3: #CBDDED
* **Reds:**
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#DE5454;'></span>Red 1 (NGUX): #DA1B28
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#EDA398;'></span>Red 2: #EDA398
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#F7D9D1;'></span>Red 3: #F7D9D1
* **Other warm colors:**
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#EB964F;'></span>Orange: #EB964F
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#FFD773;'></span>Yellow: #FFD773
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#FFF4DE;'></span>Light yellow: #FFF4DE
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#D5D94D;'></span>Yellow green: #D5D94D
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#EFE7DB;'></span>Tan: #EFE7DB
* **Other cool colors:**
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#823471;'></span>Violet: #823471
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#6F8D5C;'></span>Green: #6F8D5C
	- <span class='box' style='border:1px solid black;display:inline-block;width:25px;height:25px;margin-right:10px;background-color:#97ADBA;'></span>Blue gray: #97ADBA


[tableizer]: http://www.google.com