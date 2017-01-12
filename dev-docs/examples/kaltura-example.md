---
layout: player_example
title: Kaltura Player Integration
description: Show a prebid ad in a Kaltura player

top_nav_section: dev_docs
nav_section: quick-start

hide: true
beta: true

about:
- Using invokeVideoPlayer to set up and access the Kaltura player instance.
- Adding a Kaltura player to the page dynamically.
- Playing an ad using Kaltura's IMA3 plugin.
- Dynamically inserting a preroll ad into the Kaltura player.

player_notes:
- To begin playing ads in your Kaltura player, enable IMA ads in the Advertising section of the player page. Change the 'Request Ads' method to 'On Demand', and leave the Server URL empty. 
- To ensure that everything we need has been loaded before the player begins, we'll be inserting the player scripts and elements once bids have been returned from prebid.

jsfiddle_link: jsfiddle.net/shirleylberry/dd4wd8z7/embedded/html/
demo_link: video-demo.appnexus.com/pbjs/kaltura-prebid/kaltura-demo.html

code_lines: 149
code_height: 3200

pid: 33
---
<div markdown="1" style="top:550px" class="pl-doc-entry">
#### Line 15 to 18: Pre-define `invokeVideoPlayer`
Because we have no way of knowing when all the bids will be returned from prebid we can't be sure that the browser will reach the point where `invokeVideoPlayer` is defined before bidsBackHandler fires and tries to call it. To prevent a `invokeVideoPlayer not defined` error, we pre-define it before we make the call to prebid, and redefine it later on with the code to create the player and play the ad. In this first version it simply stores the winning vast to use later.
</div>

<div markdown="1" style="top:900px" class="pl-doc-entry">
#### Line 20 to 36: Create a video ad unit
Create a video ad unit to request bids for. The `code` is the name we'll use to refer to this ad unit throughout the prebid code. Make sure you include the `mediaType: 'video'` and replace the `placementId` with your own valid placement ID.
</div>

<div markdown="1" style="top:1200px" class="pl-doc-entry">
#### Line 38 to 54: Log the bids for debugging
Log information about the bids to the console, including whether any bids were returned. This isn't strictly necessary, but is useful for debugging.
</div>

<div markdown="1" style="top:1550px" class="pl-doc-entry">
#### Line 57 to 75: Add the ad units and request bids
Add the ad units you want to request bids for to prebid, and then call `requestBids()`, passing in a json object. In the json object, define the `bidsBackHandler` callback which will run once all the bids are returned.
</div>

<div markdown="1" style="top:1725px" class="pl-doc-entry">
#### Line 62 to 69: Build masterVideoTag and call invokeVideoPlayer
Once we have the bids back, `bidsBackHandler` will be called. Inside this callback, we create the masterVideoTag and pass it to the video player by calling `invokeVideoPlayer()`.
</div>

<div markdown="1" style="top:550px" class="pl-doc-entry">
#### Line 115 to 119: Define player settings
Create a JSON object with your account ID, the ID of your Kaltura player, and the ID of the div you're putting the player into.
</div>

<div markdown="1" style="top:550px" class="pl-doc-entry">
#### Line 122: Build player HTML
Build the HTML for your player. We're using the player settings we created above to fill in the HTML, so you should not need to change this line unless you need to change the class or data-embed attributes.
</div>

<div markdown="1" style="top:550px" class="pl-doc-entry">
#### Line 123 to 128: Add the player and Kaltura script to the page
Add the video we created above to the page. Create and add the script for your Kaltura player. Again, we're using the player settings we created earlier to fill in the script tag, so you should not need to change these lines. Once the Kaltura script has loaded, we'll create the player.
</div>

<div markdown="1" style="top:550px" class="pl-doc-entry">
#### Line 130: Initialize the player
Get a reference to the player by calling `videojs()` and passing in your player's ID. Set its `src` to the content video you want to play.
</div>

<div markdown="1" style="top:550px" class="pl-doc-entry">
#### Line 136 to 138: Play the ad
Once the player's IMA3 plugin has loaded, use the plugin to play an ad as a preroll by calling `adrequest()` and passing in the url from prebid.
</div>

<div markdown="1" style="top:3075px" class="pl-doc-entry">
#### Line 134 to 137: Account for page speed
If prebid returned bids before the browser reached the end of the page, the first version of `invokeVideoPlayer` will have been called from `bidsBackHandler` so the winning vast tag will be stored in tempTag. If that's the case, we want to call the 'real' version of `invokeVideoPlayer` with the stored url to create the player and play the ad. If `tempTag` is not defined, that means the browser reached the end of the page before the bids came back from prebid, meaning the 'real' version of `invokeVideoPlayer` was already called.
</div>

