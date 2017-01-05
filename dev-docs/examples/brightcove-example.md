---
layout: player_example
title: Brightcove Player Integration
description: Show a prebid ad in a Brightcove player

top_nav_section: dev_docs
nav_section: quick-start

hide: true
beta: true

about:
- Using invokeVideoPlayer to set up and access the Brightcove player instance.
- Adding a Brightcove player to the page dynamically.
- Playing an ad using Brightcove's IMA3 plugin.
- Dynamically inserting a preroll ad into the Brightcove player.

player_notes:
- To begin playing ads in your Brightcove player, enable IMA ads in the Advertising section of the player page. Change the 'Request Ads' method to 'On Demand', and leave the Server URL empty. 
- To ensure that everything we need has been loaded before the player begins, we'll be inserting the player scripts and elements once bids have been returned from prebid.

jsfiddle_link: jsfiddle.net/shirleylberry/dd4wd8z7/embedded/html/

code_lines: 149
code_height: 3200

pid: 32
---
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<!-- <div markdown="1">
#### Line 74: Call invokeVideoPlayer
Once all the bids are back, call invokeVideoPlayer and pass in the url. This will either store the url in the variable tempTag, or pass it to the video player.
</div> -->
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<br><br><br>
<div markdown="1">
#### Line 115 to 119: Define player settings
Create a JSON object with your account ID, the ID of your Brightcove player, and the ID of the div you're putting the player into.
</div>
<br>
<div markdown="1">
#### Line 122: Build player HTML
Build the HTML for your player. We're using the player settings we created above to fill in the HTML, so you should not need to change this line unless you need to change the class or data-embed attributes.
</div>
<div markdown="1">
#### Line 123 to 128: Add the player and Brightcove script to the page
Add the video we created above to the page. Create and add the script for your Brightcove player. Again, we're using the player settings we created earlier to fill in the script tag, so you should not need to change these lines. Once the Brightcove script has loaded, we'll create the player.
</div>
<br>
<div markdown="1">
#### Line 130: Initialize the player
Get a reference to the player by calling `videojs()` and passing in your player's ID. Set its `src` to the content video you want to play.
</div>
<br>
<div markdown="1">
#### Line 136 to 138: Play the ad
Once the player's IMA3 plugin has loaded, use the plugin to play an ad as a preroll by calling `adrequest()` and passing in the url from prebid.
</div>


