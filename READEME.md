# Install Instructions:
- You can use the same version of JQuery that you are currently using (1.12.0)
- You MUST use Bootstrap 3.0.2, instead of current Vetter bootstrap 3.3.6. Popup behavior in 3.3.6 is undesirable
- You might need to localize the * style in hover.css
- Add onresize="removePopovers()" to the body tag that will house the svg map

# Map Background Image:
In the future, if you need to recrop a different background image, I got the map from https://snazzymaps.com/style/20/gowalla

# Included Files:
- misc/baltimore-zip-map.ai - Adobe Illustrator project with Baltimore's SVG and background image
- misc/philly-zip-map.ai - Adobe Illustrator project with Philadelphia's SVG and background image
- baltimore_background.png - background image for Baltimore
- philadelphia_background.png - background image for Philadelphia
- hover.css - style for the title buttons
- svg-map.css - style for the SVG
- svg-map.js - initializes bootstrap popovers and bootstrap carousel. Also has some custom js to make popovers work smoother on all browsers.
- index.html - demo page that contains the SVG code. The whole philly-baltimore-carousel div can be cut and pasted wherever you want to display it.

# Enable a Zone
To enable a zone, start by opening the html page containing the map code. Do a search for the zip code that you want to enable. Above the zip code should be an <a ...> tag. Inside the tag there will be a bit of code that says class="btn btn-default disabled-zone". Remove the "disabled-zone" from this so the result is class="btn btn-default". This will change the zone to blue.
You also need to enable the popup that appears whenever you click the zone. In that <a ...> tag, there is a line of code that says data-content="<a href='/schedule/19112' class='centered-link disabled-popup'>19112</a>". Remove the "disabled-popup" from this code. The result will be this: data-content="<a href='/schedule/19112' class='centered-link'>19112</a>" By removing the "disabled-popup" class from that line of code, you enable the popup.

# Disabling a Zone
Follow the same steps as enabling a zone, except add "disabled-zone" to the <a ...> tag, and add "disabled-popup" to the inner popup code.
