
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






[tableizer]: http://www.google.com