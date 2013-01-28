# Featured Content Glider #

*Description:* This script lets you painlessly showcase new or featured contents on your page, by turning ordinary pieces of HTML content into an interactive, "glide in" slideshow. For the ultimate in the ability to customize its look, the pagination links are also ordinary links that you define on the page, but with special CSS class names inserted when it should perform a certain task (ie: "toc" class if it's a pagination link). It supports Youtube videos within its slides, with the help of Youtube's API.

## Directions ##

*Step 1:* This script uses the following external files:

+ jQuery 1.3 or above (served via Google CDN)
+ featuredcontentglider.js
+ featuredcontentglider.css

*Step 2:* Add the below code to the HEAD section of your page:

	<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.3.2/jquery.min.js"></script>
	
	<link rel="stylesheet" type="text/css" href="featuredcontentglider.css" />
	
	<script type="text/javascript" src="featuredcontentglider.js">
	
	/***********************************************
	* Featured Content Glider script- (c) Dynamic Drive DHTML code library (www.dynamicdrive.com)
	* Visit http://www.dynamicDrive.com for hundreds of DHTML scripts
	* This notice must stay intact for legal use
	***********************************************/
	
	</script>


*Step 3:* Then, add the below sample markup to your page:

	<script type="text/javascript">
	
	featuredcontentglider.init({
		gliderid: "canadaprovinces", //ID of main glider container
		contentclass: "glidecontent", //Shared CSS class name of each glider content
		togglerid: "p-select", //ID of toggler container
		remotecontent: "", //Get gliding contents from external file on server? "filename" or "" to disable
		selected: 0, //Default selected content index (0=1st)
		persiststate: false, //Remember last content shown within browser session (true/false)?
		speed: 500, //Glide animation duration (in milliseconds)
		direction: "downup", //set direction of glide: "updown", "downup", "leftright", or "rightleft"
		autorotate: true, //Auto rotate contents (true/false)?
		autorotateconfig: [3000, 2], //if auto rotate enabled, set [milliseconds_btw_rotations, cycles_before_stopping]
		onChange: function(previndex, curindex, $allcontents){ // fires when Glider changes slides
	  		//custom code here
		}
	})
	
	</script>
	
	<div id="canadaprovinces" class="glidecontentwrapper">
	
	<div class="glidecontent">
	<img src="http://i11.tinypic.com/8efzmmf.jpg" style="float: left; padding: 5px" />
	British Columbia is the westernmost of Canada's provinces and is famed for its natural beauty. It's capital is Victoria, located at the southeastern tip of Vancouver Island. BC's most populous city is Vancouver, located in southwest corner of the BC mainland called the Lower Mainland. 
	</div>
	
	<div class="glidecontent">
	<img src="http://i15.tinypic.com/72vilba.jpg" style="float: right; padding: 5px"/>
	Ontario is a province located in the central part of Canada, the largest by population and second largest, after Quebec in total area. Toronto, the capital of Ontario, is the centre of Canada's financial services and banking industry.
	</div>
	
	<div class="glidecontent">
	<img src="http://i17.tinypic.com/8bg0lkx.jpg" style="float: left; padding: 5px"/>
	Yukon, still commonly referred to as "The Yukon Territory", is the westernmost of Canada's three northern territories. The Yukon's major appeal is its nearly pristine nature. Tourism relies heavily on this and there are many organised outfitters and guides available to hunters and anglers and nature lovers of all sorts.
	</div>
	
	</div>
	
	<div id="p-select" class="glidecontenttoggler">
	<a href="#" class="prev">Prev</a> 
	<a href="#" class="toc">Page 1</a> <a href="#" class="toc">Page 2</a> <a href="#" class="toc">Page 3</a>
	<a href="#" class="next">Next</a>
	</div>

## Featured Content Glider set up ##

See script project page for additional details on setup and documentation: <http://www.dynamicdrive.com/dynamicindex17/featuredcontentglider.htm>
