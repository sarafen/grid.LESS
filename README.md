grid.LESS
=======

An **open** grid system for use with the LESS stylesheet language, based on, but not bound by the 960.gs

<http://bits.dezby.com/tools/grid.less/usage>

SETUP/INSTALLATION 
-----


1.) Include this plugin in the head of your style.less file with @import "/[path to folder]/grid";

3.) Add the default values to the head of your style.less file and set accordingly.

		EX:     
			
			@pw: 960px;		// Page width (best values: 720,960,1200,1560)
			@cols: 12;		// Number of columns (best values:12,16,24)
			@topd: 20px;	// Top Margin
			@padsd: 10px;	// Left & Right Padding
			

4.) Make sure your HTML markup has a "wrapper" element to hold your page content.

		EX:
			<body>
			<div id="wrapper">
			<div id="one"></div>
			<div id="two"></div>
			</div>
			</body>	
			

 4a.) Make sure your wrapper element's width is set to the page-width variable you set in the grid's default.

		EX:
			#wrapper {width:@pw;} // Doing it this way means you only have to 
                                   update once should you change the page width.
			
		
 5.) Include in your style as #ID {.col('COL#','SHRINK#','TOP MARGIN','BOTTOM MARGIN','L-R PADDING');} 

		EX:
			#one {.col(6,20px,50px,0,5px);}
			

			A div with the ID of #one spanning almost 6 columns, 
 			but you want it to stop 20px short of the 6th column right edge, and 
 			have a top margin of 50px with Left-Right padding of 5px.

 			The DEFAULT VALUES are .col(1,0,20px,0,10px);

 5a.) Push or Pull an element using the push/pull classes.
		
		EX: 
			#one {.col(6);.psh(6);}
			#two {.col(6);.pll(6);}
			

			This would switch the placement of of these two elements on a 12 col layout.

 6.) Turn the visual horizontal background grid on to check your page alignment by including the .grid(); class on your page's #wrapper element.

		EX: (Assuming your site's wrapper element is called #wrapper.)

			#wrapper {.grd;)
			

			OR set the color yourself from the default light red/pink
			
			
			#wrapper {.grid(#333);}
			

DEFINITIONS
-------

*  COL# == The number of columns you wish an element to span
*  SHRINK# == The number you wish the element to stop short of the final column's right edge
*  TOP MARGIN == The top margin of the element
*  BOTTOM MARGIN == The bottom margin of the element
*  L-R PADDING == The Left & Right Padding of the element


LICENSE
-------

See `LICENSE.txt` File.

> Copyright (c) 2011 Stephen Lovell

