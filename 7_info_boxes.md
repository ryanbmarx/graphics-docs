#Info-boxes
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

##<a name='definition-list'></a>Definition lists
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
