---
layout: player_example
title: JW Self-Hosted Player Integration
description: Show a prebid ad in a self-hosted JW Player

top_nav_section: dev_docs
nav_section: quick-start

hide: true
beta: true

about:
- Setting up JW Player to dynamically play ads.
- Using a cloud-hosted player.
- Create a masterVideoTag and pass it to invokeVideoPlayer.
- Use invokeVideoPlayer to set up and access the JW Player instance.
- Dynamically insert a preroll ad into JW Player.

player_notes:
- You must have the correct JW Player license that allows you to play advertising.
- The different methods of embedding JW Player on your site can be found <a href="https://support.jwplayer.com/customer/portal/articles/1406723-mp4-video-embed">here</a>. 
- For this example we will be using method 3, a self-hosted player and JW Platform hosted content. To see an example using the cloud-hosted player, click <a href="#">here</a>.
- No matter what embedding method you choose to use, you must follow the <b>custom embed</b> instructions. You cannot use the single-line embed.

jsfiddle_link: jsfiddle.net/shirleylberry/357yaqgc/embedded/html/
code_lines: 142
code_height: 3000

pid: 19
---
<br><br><br>
<br>
<div markdown="1">
#### Line 9 to 12: Include your self-hosted JW Player code and license key
Load the JW Player script. Open another script tag and define your license key. Replace `abcdefghijkl` with your own license key for an account that has advertising enabled. You can find your license key in your dashboard by going to Tools (found under the Players section) and scrolling to Downloads to find JW Player 7 (Self-Hosted).
</div>
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
<div markdown="1">
#### Line 119: Get a reference to the player instance
Get a reference to the player by calling `jwplayer()` and passing in the id of the div you want to load the player into.
</div>
<br>
<div markdown="1">
#### Line 129 to 136: Call setup on the player instance
Call `setup()` on the player instance with the settings you want. We need to pass in a media file and an advertising block with a `client` defined.
</div>
<div markdown="1">
#### Line 126 to 128: Pass in Advertising
We must pass in an `"advertising"` block in our settings in order to enable advertising for this player. We can also specify the tag or an ad schedule here but for this demo we'll insert the tag dynamically before the content plays.
</div>
<div markdown="1">
#### Line 131 to 133: Play a prebid ad as a preroll
Before the player begins to play the content video, play an ad.
</div>


