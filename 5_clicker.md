#Use the "clicker," a.k.a. makePanels.js

##Start with our base CSS

	<link rel="stylesheet" type="text/css" href="http://photodesk.chicagotribune.com.s3.amazonaws.com/graphics-toolbox/tribune-graphics-base-1.0.min.css">

##You'll need these javascript libraries:

	<script type='text/javascript' src="http://code.jquery.com/jquery-2.1.1.min.js"></script>
	<script type="text/javascript" src='http://photodesk.chicagotribune.com.s3.amazonaws.com/graphics-toolbox/makePanels/jquery.makePanels.1.0.min.js'></script>
##You'll need this css library:
	
	<link rel="stylesheet" type="text/css" href="http://photodesk.chicagotribune.com.s3.amazonaws.com/graphics-toolbox/makePanels/jquery.makePanels.1.0.min.css">
##Structure your HTML like this:

	<div id='something-unique'>
		<div id='something-else-unique' class='panel' data-btn-label ='This is the label'>
		...
		</div>
	</div>
The overall wrapper needs a unique ID, as does each panel within it. The `data-btn-label` attribute for each panel is the text that will be used in the buttons or dropdown menu.

##Use this javascript. 
Generally, all your javascript need only be inside one `<script>` tag

	<script type="text/javascript">
	$('#something-unique').makePanels({
		type:"dropdown", 	/* Options are "none", "buttons" or "dropdown" */
		transitionSpeed: 150, /* 0=instant, 1000 = 1 second */
		showForwardBackButtons:true, /* duh! */
		alignNav:"center" /* Also can be "left" */
	});
	</script>

The biggest decision you'll have is what kind of navigation you want. You have three options.

* Just forward and back buttons. This is the default.
* A dropdown showing all the `data-btn-label` information
* Individual tabs, each showing `data-btn-label` information