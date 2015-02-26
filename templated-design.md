#Make a templated design
This is another one of those things that you should work with Ryan on.

	<script type='text/javascript' src="//code.jquery.com/jquery-2.1.1.min.js"></script>
	<script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/underscore.js/1.7.0/underscore-min.js"></script>
	<script type="text/javascript" src="//photodesk.chicagotribune.com.s3.amazonaws.com/graphics-toolbox/underscore.csvtojson.js"></script>

This script helps:

	<script type="text/javascript">
		/* MAKE IN IIFE -- THE NAME WILL BE THE NAMESPACE PREFIX */
		var freeAgents = (function ($) {
			/* ANYTHING FUNCTION OR VARIABLE WANT EXPOSED NEEDS TO BE AN ELEMENT OF THIS OBJECT */
			var myObject = {};

			myObject.publicFunctionName = function (args) {};
			var privateFunctionName = function(args) {}

			/* THIS IS A BASIC FORMAT FOR GRABBING GOOGLE DATA AND TEMPLATING IT */
			var pullData = function (sheet, tab) {
				$.get('https://spreadsheets.google.com/feeds/list/'+ sheet +'/' + tab +'/public/values?alt=json', function(data){
					var templateText = _.template($('#freeagentTemplate').html()),
					parsedTemplate = "";
					for(var i=1; i<data.feed.entry.length; i++) {
						parsedTemplate += templateText(data.feed.entry[i]);
					}
					$('#target').html(parsedTemplate).change();
				}).error(function(){
					alert('There was a problem loading the data. Please refresh the page!');
				});
			};
			pullData (GOOGLE SHEET KEY,TAB NUMBER);
			/* THIS EXPOSES FUNCTIONS*/
			return myObject;
		})(jQuery);
	</script>
	<script id='template' type="text/template"></script>