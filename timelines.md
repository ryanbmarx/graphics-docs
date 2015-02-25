#A standard timeline 
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
