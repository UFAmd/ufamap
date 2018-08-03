# ufamap
Editing Instructions

Edit by opening the file that needs changes in a text editor, making changes, and replacing the old file with the changed one. 

To add a user dot:
In "index.html" find the section within the svg that applies to the user (academic, international, etc).
Copy and paste the following into that section: 

  <circle class="pin" class=""
            cy=""
            cx=""
            fill=""
            name=""
            r=".35%" info=""
            picture="" att="" atc="" ats="" atv="" atr="" />
 
 Set the "class" attribute to the user type. For example, class="faa" (for faa academic users).
 Use google maps or a similar service to find the latitude and longditude of the user location. Set cy to the latitude and cx to the    longditude.
 Set fill to the same hex code as the other users in that section (or if it's an international user, or doesn't fit into another section, choose a hex code for it. You can find hex codes at htmlcolorcodes.com.
 Set name to the title that you want the user's popup box to display. Set info to any subtitle you want for the popup box.
 Set the product attributes according to which products the user has. If the user has the product, set the attribute to 0. If they do not, set it to 80. So, if the user uses ATTower, set att="0". If they do not have ATCoach, set atc="80". Do the same for each attribute (ATSpeak, ATView, ATRadio). 
 Change the picture attribute to the file name of the picture you want the popup to show when you click that pin. Make sure to save the new photo to the file. 
 An example of a completed user pin:
   <circle class="pin" class="faa"
            cy="61.218"
            cx="-149.858"
            name="University of Alaska, Anchorage"
            fill="#BBDEFB"
            r=".35%" info="Aviation Technology Division"
            picture="uak.jpg" att="0" atc="80" ats="80" atv="80" atr="80" />
           
To change the color of all pins in a section, figure out what the hex code is for the fill on that section, ctrl+h and replace with the new color code. 

To change the size of the pins, ctrl+h and replace r=".35%" with the new value (ex. r=".25%")

To change the background appearance of the map, open 'miller-cropped.svg' and find the tag near the top that says <style type="text/css">.
There will be a list of attributes as follows:
	.st0{fill:#DCDCDD;stroke:#4C5C68;stroke-width:.75;stroke-miterlimit:3.9745;}
	.st1{fill:#DCDCDD;stroke:#4C5C68;stroke-width:0.75;stroke-miterlimit:3.9745;}
	.st2{fill:#DCDCDD;}
	.st3{fill:#DCDCDD;fill-opacity:0;}
	.st4{fill:#C5C3C6; stroke:#4C5C68;stroke-width:0.75;stroke-miterlimit:3.9745;}

Change the land color by replacing the hex code used for the fill: value on .st0 through .st3 with the new hex code. 
Change the border color by replacing the hex code used for the stroke: value on .st0 through .st3 with the new hex code. 
Change the weight of the lines by changing the stroke-width: values on .st0, .st1, and .st4.

Change the background color by opening pagestyle.css and finding the #map section. Change the hex code on the background-color attribute.

To change the appearance of the popup window, open pagestyle.css. 
Change the color by changing the background-color attribute in the #modal tag. 
Change the title color by changing the color attribute in the #modal-header tag. 
Change the text color by changing the color attribute in the #modal-body tag.
Change the font family by adding a font-family attribute to both the #modal-body and the #modal-header tag and entering the font family you want to use. 
Change the close button color by changing the color attribute on the closeBtn tag. 
Change the hover color of the close button by changing the color attribute in the #closeBtn:hover tag.

To change the style of the tooltip text (which pops up when you hover over a pin), open the pagestyle.css file and change the fill, stroke, font-size, font-family attributes. 
